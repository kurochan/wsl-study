# 第1回WSL勉強会

#### 2013/8/2

## テーマ: VM環境の構築とJava
8/7の数理最適化研究室勉強会のための準備(VM環境構築)と、要望が多かったJavaの復習やりましょう


## 全体の流れ
1. どんな感じで勉強会をやっていくか
1. VM環境の構築
1. Java勉強会#1

## どんな感じで勉強会をやっていくか
* どうして勉強会をしたいのか
    * セキュリティ＆プログラミングキャンプの影響
    * ハッカー文化に触れたい
* どんな感じでやっていくか、軽く話し合って決めましょう

## VM環境の構築
* できるところまでやってきてもらった方がいいかも
    * 構築するだけだからわからない所あったらサポートする感じで

### 構築方法 (Windows機の人)
VirtualBoxっていう仮想化ソフトと、LinuxのディストリビューションであるUbuntuを組み合わせて使います。

#### VirtualBoxのダウンロード
https://www.virtualbox.org/wiki/Downloads から

* VirtualBox x.x.xx for Windows hosts
* VirtualBox x.x.xx Oracle VM VirtualBox Extension Pack

をダウンロードする。

#### Ubuntuのダウンロード

http://www.ubuntu.com/download/desktop から

* Ubuntu 13.04 32-bit(64bit版が使いたい人はいいけど、とりあえず最初は32bit版使うのが無難な気がする)

↑を選択した後、ページ下の"Not now, take me to the download"ってやつクリックすればダウンロードが始まるはず。

#### VirtualBoxのインストール

#### VirtualBoxにUbuntuをインストール

#### 仮想マシンに必要なソフトウェアのインストール

    $ sudo apt-get install build-essential

## Java勉強会#1
* そもそもJavaって何だ？
    * Javaってどんな言語？
    * Javaのコミュニティ
    * 中間言語
        * バイトコードをのぞいてみる？
    * VM
        * Androidはどうなってる？
    * GC
        * アルゴリズム
* 基本文法
    * 教科書に載ってそうなこと
    * 一応日本語使えるよ
    * オートボクシング
    * シンタックスシュガー
* オブジェクト指向
    * オブジェクトクラス
* オーバーライドとオーバーロード
    * できると何がいいの？
* デザインパターン
    * ゲッターとセッター
    * シングルトン
* シャローコピーとディープコピー
* 並列プログラミング
    * 副作用のある関数とない関数
    * 排他制御
        * デッドロックって？
* 標準ライブラリ
    * StringBuilder / StringBuffer
* 外部ライブラリ
    * twitter4jの紹介
* <del>JavaリフレクションAPI</del>
    * 最初は知る必要ないかも
* Javadocの読み方
    * http://docs.oracle.com/javase/jp/6/api/
* サーブレット
    * tomcat
* 分散処理
    * Hadoopの紹介(配達先輩に喋ってもらう？)
* コーディング技術
    * 300行→1,000行→10,000行
    * リファクタリング
    * コーディング規約
    * ペアプロ
* テスト
    * ソースコードの信頼性について
    * JUnit
    * カバレッジ計測
    * テストによるモチベーションの維持
* 開発手法について
    * TDD
* テーマを設けてプログラムを作ってみる
    * 時間あるかな？
    * 文章を自動生成するプログラムを作ってみる
        * https://twitter.com/asshuku
        * https://twitter.com/shuumai
    * 用意されたJavadocに沿って実装してみる？

## メモ
