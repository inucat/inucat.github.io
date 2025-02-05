---
layout: post
# quote required
title: "用語集 - enPiTでのチーム開発経験を語りたい"
# description:
# yyyy-mm-dd hh:mm
# created_date: 2025-01-31 00:45
# category
tags: [enpit, development, agile, teamwork, appendix]
---

# enPiT でのチーム開発経験を語りたい - 用語集

本文で用いる、あるいは関連する用語で、特に筆者が必要と判断したものを列挙しています。
正確な語義というよりも本文中での筆者の解釈という性質が強いです。

- 参考資料
  - [Agile Glossary and Terminology - Agile Alliance ➚][agile-glossary]

[agile-glossary]: https://www.agilealliance.org/agile101/agile-glossary/

---

- [enPiT でのチーム開発経験を語りたい - 用語集](#enpit-でのチーム開発経験を語りたい---用語集)
  - [CI/CD](#cicd)
  - [CRUD](#crud)
  - [Docker](#docker)
  - [enPiT](#enpit)
  - [Git](#git)
  - [GitHub](#github)
  - [JavaScript](#javascript)
  - [React](#react)
  - [Miro](#miro)
  - [Next.js](#nextjs)
  - [ORM](#orm)
  - [Prisma ORM](#prisma-orm)
  - [Scrapbox](#scrapbox)
  - [SQL](#sql)
  - [TypeScript](#typescript)
  - [Vercel](#vercel)
  - [アジャイル開発 agile development](#アジャイル開発-agile-development)
  - [イシュー issue](#イシュー-issue)
  - [インクリメンタル incremental](#インクリメンタル-incremental)
  - [オープンソース open source](#オープンソース-open-source)
  - [コード整形ツール code formatter](#コード整形ツール-code-formatter)
  - [コンテナ container](#コンテナ-container)
  - [シンギュラリティ singularity](#シンギュラリティ-singularity)
  - [スーパーこよみ Super Koyomi](#スーパーこよみ-super-koyomi)
  - [スクラムマスター scrum master](#スクラムマスター-scrum-master)
  - [スプリント sprint](#スプリント-sprint)
  - [スプリントバックログ sprint backlog](#スプリントバックログ-sprint-backlog)
  - [生成 AI generative artificial intelligence](#生成-ai-generative-artificial-intelligence)
  - [セルフホスト self-host](#セルフホスト-self-host)
  - [ソフトウェアアーキテクチャ software architecture](#ソフトウェアアーキテクチャ-software-architecture)
  - [データベース database](#データベース-database)
  - [テスト test](#テスト-test)
  - [デプロイ deploy](#デプロイ-deploy)
  - [ブランチ branch](#ブランチ-branch)
  - [フルスタック full-stack](#フルスタック-full-stack)
  - [プルリクエスト PR, pull request](#プルリクエスト-pr-pull-request)
  - [フレームワーク framework](#フレームワーク-framework)
  - [プロダクトオーナー product owner](#プロダクトオーナー-product-owner)
  - [プロダクトバックログ product backlog](#プロダクトバックログ-product-backlog)
  - [プロダクトバックログアイテム product backlog item](#プロダクトバックログアイテム-product-backlog-item)
  - [ペアプログラミング pair programming](#ペアプログラミング-pair-programming)
  - [リポジトリ repository](#リポジトリ-repository)
  - [リリースノート release note](#リリースノート-release-note)

---

## CI/CD

「コードの品質を高い状態に保つこと」と、「動くソフトウェアだけがデプロイされる状態を保つこと」の 2 点を目指して、
ビルド、テストやデプロイをコンピュータで自動化して、開発効率を向上する取り組み。
Continuous integration and Continuous deployment の略。

## CRUD

アプリケーションがしばしば遭遇するデータ処理。
create、read、update、delete の頭文字をとったもの。

## Docker

コンテナ技術。
Linux のプロセス隔離の技術を巧みに利用して使いやすく提供することで不動の人気を獲得した。
コンテナ界隈の事実上の標準。

<!-- - [Docker ➚](https://www.docker.com/) -->

## enPiT

文部科学省が推進した情報技術人材の育成のための取り組み。現在は各大学・企業が自主的に協力して教育プログラムを提供している。

## Git

超人 Linus Torvalds らにより開発された分散バージョン管理システム。
リモートのリポジトリから適宜手元の環境へ複製してローカルのリポジトリを作り、手元の環境で別々に変更履歴を管理できるので、
SVN などと異なりリモートへの影響少なく複数人での共同作業がしやすい。

<!-- - [Git ➚](https://git-scm.com/) -->

## GitHub

Git のリモートリポジトリを提供し、その管理用 Web インタフェースを提供するサービス。Git ホスティングサービスの中では代表的存在である。

## JavaScript

当時の Java 人気に便乗して LiveScript から改名した節操のない言語。
生息域も節操無しで、ブラウザでも OS 上でも動く。

## React

Web アプリケーション開発のフレームワーク。

<!-- - [React ➚](https://react.dev/) -->

## Miro

付箋を貼ったり、表を作ったりといった共同作業のできるホワイトボードアプリケーション。
計算資源の消費が激しく、非常に動作が緩慢なので大人数では役に立たない。WASM で高速化できないものかしら。

<!-- - [Miro ➚](https://miro.com/ja/) -->

## Next.js

React 開発のフレームワーク。
React と融合してブラウザ側からサーバ側まであらゆる段階の処理を記述する、いわゆるフルスタック（full-stack）開発を支援する。

<!-- - [Next.js ➚](https://nextjs.org/) -->

## ORM

Object-Relation Mapping の略。
データベースとプログラミング言語とではデータ表現形式や CRUD 手続きが異なり、それらを対応させてプログラムから扱いやすくするための技術。
SQL 文の自動生成機能があると大変便利。

## Prisma ORM

ORM の一つ。
データベース中のデータに関する型定義を提供してくれるので、TypeScript と相性が良い。

## Scrapbox

文章の形で共同編集ができるオンラインサービス。
同期的な Wiki と考えて差し支えないかも知れない。
最近名前が変わったらしい。

## SQL

Structured Query Language の略。
データベースにおいてデータの定義や操作を表した言語。
なんとなく、プログラミング言語より難しい雰囲気がある。
~~自然言語にすり寄った言語は難しい。~~

## TypeScript

JavaScript を拡張して、型を扱えるように設計されたプログラミング言語。
変換器を通じて JavaScript ファイルに変換して、JavaScript 実行環境で動かす。
TypeScript ではこの変換器のことをコンパイラ（compiler）と呼び、変換のことをコンパイル（compile）と呼ぶ。

## Vercel

Web アプリケーションのホスティングサービス。

<!-- - [Vercel ➚](https://vercel.com/) -->

## アジャイル開発 agile development

ソフトウェア開発手法の 1 つ。
既存の手法に対して「対話・顧客との協調・動く成果物・変化への柔軟性」などへより重きをおいている。
特に対話を通じて手法自体を点検して、チームにとって最善の手法を追求することで継続的に価値を提供できることを目標とする。

## イシュー issue

バグ追跡システム（bug tracking system, BTS）において、一つひとつのバグ報告のこと。
GitHub などは BTS を内包しているので、通常は GitHub のイシューなどという。
バグ報告の他、機能リクエストや使用方法の質問などもイシューを通して行われる場合もある。

## インクリメンタル incremental

（incremental development の形で）リリースされたどの状態でもそのソフトウェアが利用できる状態で、
かつ後のリリースは前のリリースよりも機能が追加・向上されていること。
インクリメントは `i++` などのプログラミングの用語なので、直感的だと思う。

## オープンソース open source

ソフトウェアのソースコードを公開する取り組み。
一般にはソフトウェアのソースコードは **著作権で保護されている** ため、無闇に複製などしてはならない。
しかしオープンソースといえば、 **著作権者の権利行使として** 著作権者などが定める一定の条件のもとに自由な利用が許諾されている。

## コード整形ツール code formatter

ソースコードの細かな体裁を一定規則のもとで統一するためのソフトウェア。
共同開発では、Git での差分を減らしたり、インデントなどの書式を揃えて相互理解を簡単にしたりするなどの利点がある。

## コンテナ container

VM のような、一定程度に隔離されたアプリケーション実行環境。

→ [Docker](#docker)

## シンギュラリティ singularity

AI の文脈においては、AI が人間の知的能力を上回るとされる時点。
著名な AI 研究者 Ray Kurzweil はそれを [2045 年と予測している ➚][singularity]が果たして……？

[singularity]: https://en.wikipedia.org/wiki/The_Singularity_Is_Near

## スーパーこよみ Super Koyomi

筆者が属する enPiT 参加チームの名前。同時に、我々が制作した日程調整支援アプリケーションの名前でもある。

- [チーム「スーパーこよみ」 ➚](https://github.com/enpit-super-koyomi)
- [すーぱーこよみ Web アプリ ➚](https://superkoyomi.org/)

## スクラムマスター scrum master

開発チームの中で、チームがアジャイル開発の精神で動くこと、チームで合意された方法で動くことを促進する役割。
おそらく開発の方向性や方法論について説くなど、PO よりも抽象度の高い仕事をする。
SM、ScM とも。

## スプリント sprint

1 つの価値創造を達成するまでの開発周期の単位。

## スプリントバックログ sprint backlog

スプリント中に完成させたい機能・変更点・バグ修正など。
プロダクトバックログの部分集合。

## 生成 AI generative artificial intelligence

文章／画像／音楽など、人間の高度な知的行動を学習して、それらの分野で一定水準のコンテンツを生成しうる人工知能。

## セルフホスト self-host

漢のロマン。

## ソフトウェアアーキテクチャ software architecture

巨大・複雑なソフトウェアの設計において定めるべきソフトウェアの構造。
ソフトウェアの機能や要素ごとに分割して、各部分の関係を整理するために用いる。
ネットワーク通信では層構造、
Web アプリケーションなどの GUI においては MVC モデルが一般的に採用される。

## データベース database

データを構造的・体系的に管理して、効率よく読み書きや検索を行えるようにしたもの、あるいはその技術。
数学的な理論が濃縮されている。
本文では特に表（table）でデータを管理する「関係データベース」を指すものとする。

## テスト test

ソフトウェア開発では、対象ソフトウェアの振る舞いが開発者の期待通りであるかを検証するためのプログラムを指す。
たとえば、HTTP サーバに対するテストでは、存在しないページを要求されたら 404 を返せるかどうかを検証する、など。

## デプロイ deploy

作成したソフトウェアを、公衆の利用に供すること。
多くは、サーバ上へのサービスの展開を意味する。

## ブランチ branch

Git において、リポジトリの特定の状態から分岐した履歴を示すマーカー。

## フルスタック full-stack

見た目側（フロントエンド、front-end）とサーバ側（バックエンド、back-end）の両方を合わせたものを指す。
full-stack enginner といえば、前後を統べるエンジニアのこと。隙がない。

## プルリクエスト PR, pull request

Git において、手元で行った変更をリモートのリポジトリへ取り込みたい、あるいは取り込んでくれという要求のこと。
共同開発では、この段階で他メンバが変更をレビュー（review）して、PR を承認したり更なる変更を要求したりできる。

## フレームワーク framework

プログラム中から呼び出される単なるライブラリから一歩進んで、プログラムの書き方・構成までを規定するように規模を拡大したソフトウェア部品。
単なるライブラリよりも多機能だが学習曲線も急になる。

## プロダクトオーナー product owner

開発チームの中で、目標を達成するために PBL を管理・調整する役割。
おそらく PBI の粒度調整や優先度管理など、ScM よりも開発寄りの仕事をする。
PO とも。

## プロダクトバックログ product backlog

プロダクトを通して提供したい新機能・変更点・バグ修正など。
一般的に開発段階の進展とともに増えていく。
PBL とも。

## プロダクトバックログアイテム product backlog item

PBL を構成する各項目。
これをいかに細分化するかが納期達成の鍵と言える。
PBI とも。

## ペアプログラミング pair programming

2 人で同じ画面を見てプログラムを書いていくこと。ペアプロ。
具体的には一人がキーボードを叩いて、もう一人はなるべく指示にまわるようにして、その役割を交代していくものとされる。

なお、さらに人が増えるとモブプログラミング、モブプロと呼ばれる。

## リポジトリ repository

バージョン管理システムにおいて、ソースコードの置き場所を指す単語。
手元の環境にあるものをローカル（local）、別のコンピュータ上にあるものをリモート（remote）と呼び区別することがある。

## リリースノート release note

ソフトウェアの新バージョン公開ごとに変更点をユーザに示す文書。
「軽微な修正」という中身のないものから「XX を追加して YY できるようになりました」というユーザ目線の利益を述べるものまで様々ある。
アジャイル開発では、リリースごとにユーザ目線の利益を具体的に記述できることが理想的。
