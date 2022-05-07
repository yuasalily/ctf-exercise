### Description
拡張子がないファイルを貰ってこのファイルを実行しろと言われたが、どうしたら実行出来るのだろうか。
この場合、UnixやLinuxのとあるコマンドを使ってファイルの種類を調べて、適切なOSで実行するのが一般的らしいが…

### Writeup
ダウンロードしたファイルを実行するとflagが得られる。


### memo
ファイルの種類はLinuxの`file`コマンドで確認できる。今回の場合だと

`file -i exec_me`

とすれば

`exec_me: application/x-sharedlib; charset=binary`

と出てくる。これで実行可能なファイルだとわかる。

ファイル形式を判定するものだと[こんなサイト](http://ixtlilton.net/cgi/FileMimeChk.cgi)もある。

`file warm`

とすれば

`exec_me: ELF 64-bit LSB executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 2.6.24, BuildID[sha1]=663a3e0e5a079fddd0de92474688cd6812d3b550, not stripped`

と表示され'elf'ファイルだとわかる。

`elf`ファイルは`readelf`で情報を表示できる。

- ELFとは
  - [ITmedia](https://www.itmedia.co.jp/help/tips/linux/l0448.html)
  - [Wikipedia](https://ja.wikipedia.org/wiki/Executable_and_Linkable_Format)
  - [もう少し詳しく](https://sugawarayusuke.hatenablog.com/entry/2017/04/09/213133)
