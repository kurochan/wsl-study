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
    * Ubuntu 13.04がうまく動かなかった人もいるので、現時点での安定版(12.04LTS)を使うのが無難かもしれません。

↑を選択した後、ページ下の"Not now, take me to the download"ってやつクリックすればダウンロードが始まるはず。

## VirtualBoxのインストール

## Extension Packのインストール

## VirtualBoxにUbuntuをインストール
別の所に書いておきました。  
http://kurochan-note.hatenablog.jp/entry/2013/07/28/130739

## 数理最適化研究室勉強会のための準備
###エディタを入れましょう。

```sh
$ sudo aptitude install vim
```

###TeXの環境構築をしましょう。  
インストール(そこそこ時間がかかります)

```sh
$ sudo aptitude install texlive-lang-cjk latexmk
```

設定

```sh
$ sudo vim /usr/bin/latexmk
```

それぞれ、  
`$latex = 'latex %O %S';` を `$latex = 'platex %O %S';` に  
`$dvipdf = 'dvipdf %O %S %D';` を `$dvipdf = 'dvipdfmx %O %S;'` に  
`$pdf_mode = 0;` を `$pdf_mode = 3;`に  
置換します。
