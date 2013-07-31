# Java勉強会#1


## そもそもJavaって何だ？
Java Day Tokyo2013の基調講演資料
> http://otndnld.oracle.co.jp/ondemand/javaday/L-1.pdf


### Javaってどんな言語？
Javaの精神

> "Write once, run anywhere"

Java Day Tokyo2013の初心者向けセッション

> http://otndnld.oracle.co.jp/ondemand/javaday/J-4.pdf

###  Javaのコミュニティ
日本Javaユーザーグループ

> http://www.java-users.jp/

###  中間言語
#### バイトコードをのぞいてみる？

```sh
$ od HelloWorld.class
$ od -c HelloWorld.class
```

#### デコンパイルしてみよう！

```sh
$ javap -c -l -v HelloWorld
```

### VM

#### クラスロードの様子を見てみる

```sh
$ java -verbose:class HelloWorld
```

#### 最適化がある時 / ない時
ない時

```sh
$ java -Xint [クラス名]
```

ある時

```sh
$ java [クラス名]
```

### セキュリティ
### Androidはどうなってる？
Androidのアーキテクチャ(日本Android友の会資料)  

> http://www.android-group.jp/index.php?plugin=attach&pcmd=open&file=RIA-Android.pdf&refer=%B5%BB%BD%D1%BB%F1%CE%C1

### GC
ガーベジコレクションの略。  
使用しなくなったオブジェクトの開放を自動でやってくれる。  
プログラマが明示的にメモリの確保や開放といった処理を記述しなくてよい。  
メモリリークを回避できる。

#### アルゴリズム
* 参照カウンタ
    * 循環参照の問題がある(Weak Referenceによる解決方法もある)
* マーク・アンド・スイープ
    * 保守的なGCと呼ばれる
* コピーGC
    * メモリサイズが使う量の2倍必要
    * コンパクションも一緒にできる
* 世代別GC
* Stop the World / Concurrent

#### GCの様子を見てみる

```sh
$ java -verbose:gc [クラス名]
```

### Javaって万能なの？
#### Rubyと比較してみよう！

## 基本文法
### 教本を読んでみよう
「やさしいJava」を例に

* mainメソッド
* 標準出力
* トークン
    * リテラル, キーワード, 識別子, 演算子, 区切り子
    * http://ja.wikipedia.org/wiki/%E3%82%AD%E3%83%BC%E3%83%AF%E3%83%BC%E3%83%89_(Java)
* 標準入力
* エスケープシーケンス
* 変数の宣言 `型名 識別子;`
* 変数代入 `変数名 = 式;`
* 演算子 `(), [], ., ++, --, !, ~, +, -, new, *, /, %, <<, >>, >>>, >, >=, <, <=, instanceof, ==, !=, $, ^, |, &&, ? :, =`
* 条件分岐
    * if, switch
* 繰り返し
    * for, while, do-while
* 配列
* クラス, オブジェクト
* メンバ変数, メソッド
* アクセス制限
* インターフェース
* 例外
* スレッド

### 拡張for文
for文のシンタックスシュガー

```java
for(Object obj : array) {
    System.out.println(obj);
}
```

### オートボクシング
### 一応日本語使えるよ
日本語プログラミングの例  
https://gist.github.com/kurochan/1164946  
ここからわかるように、変数やクラス名といったものに日本語(マルチバイト文字)を用いるのは適切ではない。

## デバッグのしかた
* eclipseを例にとって

## オブジェクト指向
### すべてのオブジェクトはオブジェクト型を継承している

### 型システム
### オブジェクトクラス
### シャローコピーとディープコピー
知らないとハマりますよ  
http://kurochan-note.hatenablog.jp/entry/20110316/1300267023

## オーバーライドとオーバーロード
### できると何がいいの？


## インターフェイス
### 多重継承ができる
### 引数と戻り値はインターフェイスとして実装するべき
### インターフェイスには名前空間がない


## パッケージ
### 名前空間
### なぜパッケージ名はドメイン名なのか
歴史的な経緯がある。  


## 例外
### 暗黒面
RuntimeExceptionのサブクラスは絶対に作ってはいけない


## デザインパターン
### ゲッターとセッター
### シングルトン


## 並列プログラミング
### 副作用のある関数とない関数
### 排他制御
#### デッドロックって？


## 標準ライブラリ
### StringBuilder / StringBuffer
### コレクション系
#### List系
#### Set系
#### Map系


## 外部ライブラリ
### twitter4jの紹介


##  <del>JavaリフレクションAPI</del>
最初は知る必要ないかも


## Javadocの読み方
> http://docs.oracle.com/javase/jp/6/api/


## サーブレット
### tomcat


## 分散処理
> http://otndnld.oracle.co.jp/ondemand/javaday/C-4.pdf

### Hadoopの紹介(配達先輩に喋ってもらう？)


## コーディング技術
### 300行→1,000行→10,000行
### リファクタリング
### コーディング規約, コーディングスタイル
### ペアプロ


## テスト
### ソースコードの信頼性について
### JUnit
### カバレッジ計測
### テストによるモチベーションの維持
#### 個人で開発する時と、チームでプロジェクトとしてやるときのモチベーションの違い


## 開発手法について
### TDD

## テーマを設けてプログラムを作ってみる
### 時間あるかな？
### 文章を自動生成するプログラムを作ってみる

>
* https://twitter.com/asshuku
* https://twitter.com/shuumai

### 用意されたJavadocに沿って実装してみる？
