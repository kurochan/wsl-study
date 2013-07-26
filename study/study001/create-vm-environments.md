# VM環境の構築 (Windows機の人向け)
VirtualBoxっていう仮想化ソフトと、LinuxのディストリビューションであるUbuntuを組み合わせて使います。

## VirtualBoxのダウンロード
https://www.virtualbox.org/wiki/Downloads から

* VirtualBox x.x.xx for Windows hosts
* VirtualBox x.x.xx Oracle VM VirtualBox Extension Pack

をダウンロードする。

## Ubuntuのダウンロード

http://www.ubuntu.com/download/desktop から

* Ubuntu 13.04 32-bit(64bit版が使いたい人はいいけど、とりあえず最初は32bit版使うのが無難な気がする)

↑を選択した後、ページ下の"Not now, take me to the download"ってやつクリックすればダウンロードが始まるはず。

## VirtualBoxのインストール

## Extension Packのインストール

## VirtualBoxにUbuntuをインストール

## 仮想マシンの起動

## とりあえずアップデートかけとく
ターミナルを立ち上げて、以下のコマンドを入力。

```sh
$ sudo apt-get update
```

最初はそこそこ時間かかるかもしれないので、気長に待ちましょう。

## 仮想マシンに必要なソフトウェアのインストール
ターミナルを立ち上げて、以下のコマンドを入力。

```sh
$ sudo apt-get install build-essential
```
