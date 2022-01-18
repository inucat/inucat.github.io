# 外付け光学ドライブ
External DVD+-R/RW Drive を接続するための Slimline SATA <-> USBケーブルを入手した。
KDE neonで認識されたが、認識されるまでにいくつか処置が必要だったため備忘録を残す。

## ライブラリのインストール

`sudo apt install libcdio18 libcdio-cdda2 libisofs growisofs`

※必要十分のパッケージかどうかは不明。

## 再起動

VLCにて再生可能になった。
