---
layout: post
title: "macOSでlogrotate"
created_date: 2024-12-13
---

- [logrotate](#logrotate)
  - [Installation](#installation)
  - [Configuration](#configuration)
    - [全体設定](#全体設定)
    - [サーバごとの個別設定](#サーバごとの個別設定)
    - [サービスの有効化](#サービスの有効化)

# logrotate

> The logrotate utility is designed to simplify the administration of
> log files on a system which generates a lot of log files. Logrotate
> allows for the automatic rotation compression, removal and mailing
> of log files.

[logrotate ↗️][1]は、サーバのログ管理に重宝する道具です。
macOS 上で Dovecot のログの切り替えのために使ってみました。

[1]: https://github.com/logrotate/logrotate

## Installation

MacPorts を使うなら:

```
# port install logrotate
```

## Configuration

設定が必要です。

### 全体設定

まず設定ファイルで /opt/local/etc/logrotate.d が include されることを確認します。

```conf
# /opt/local/etc/logrotate.conf
# -----------------------------
# 詳細は `man logrotate` で確認ください。
# 毎週ログを切り替えします。
weekly
# 4周回分（上記と合わせると、すなわち4週間分）だけ保存します。
rotate 4
# 切り替え後は新しい空のログファイルを作成します。
create
# 切り替え済みのログファイルの末尾に日付を記します。
dateext
# ログを圧縮します。
compress
# 個々の設定スクリプトは下記のディレクトリに追加して下さい。
include /opt/local/etc/logrotate.d
```

### サーバごとの個別設定

個別のアプリケーションに対しては logrotate.d ディレクトリ下に設定を書きます。
個別設定は全体設定に、後に現れる設定は先に現れる設定にそれぞれ優先します。

Dovecot の例（[公式文書そのまま ↗️][2]）:

[2]: https://doc.dovecot.org/2.3/admin_manual/logging/#rotating-logs

```conf
# /opt/local/etc/logrotate.d/dovecot
# ----------------------------------
/opt/local/var/log/dovecot.log {    # 対象とするログファイル。
    weekly
    rotate 4
    missingok           # ログファイルが存在しない場合をエラーとしては扱わない。
    notifempty          # ログが空の場合は切り替えを行わない。
    compress
    delaycompress       # ログの圧縮を次回の切り替え時まで遅延する。
    sharedscripts       # 複数のログ切り替えの際も、スクリプトを一度のみ走らせる。
    postrotate          # 切り替え後（post rotate）に実行されるスクリプト。
        # 内容。/bin/sh により実行される。インデントは任意。
        # MacPorts 由来のコマンドは、PATH の関係上絶対パスで書くことをおすすめ。
        #
        # > マスタープロセスへ SIGUSR1 を送り、ログファイルを再読み込みさせる。
        # > -- doveadm-log(1) より
        /opt/local/bin/doveadm log reopen
    endscript           # スクリプト終了。
}
```

### サービスの有効化

MacPorts でインストールされた logrotate には launchd 用の構成ファイルが存在します。
したがって、次のように logrotate サービスを有効化すれば、自動で起動して定期的に実行されます。

```
# port load logrotate
```

なお、提供されるファイルは次のようなものです。

```xml
<!-- /opt/local/etc/LaunchDaemons/org.macports.logrotate/org.macports.logrotate.plist -->
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
    <key>Disabled</key>
    <true/>
    <key>Label</key>
    <string>org.macports.logrotate</string>
    <key>ProgramArguments</key>
    <array>
        <string>/opt/local/sbin/logrotate</string>
        <string>/opt/local/etc/logrotate.conf</string>
    </array>
    <key>StartCalendarInterval</key>
    <dict>
        <key>Hour</key>
        <integer>5</integer>
        <key>Minute</key>
        <integer>30</integer>
    </dict>
</dict>
</plist>
```
