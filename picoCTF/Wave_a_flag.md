### Description
Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...

### Writeup
ダウンロードしたファイルをとりあえずエディタで開くとわけのわからないものが出てくる。

まず間違いなくバイナリファイルだと思うので`./warm`と実行すると`-h`を付けるといいよみたいなものが出てくる。そこで`./warm -h`と実行するとflagを得られる。


### memo
ファイルの種類はLinuxの`file`コマンドで確認できる。今回の場合だと

`file -i warm`

とすれば

`warm: application/x-sharedlib; charset=binary`

と出てくる。これで実行可能なファイルだとわかる。

ファイル形式を判定するものだと[こんなサイト](http://ixtlilton.net/cgi/FileMimeChk.cgi)もある。

バイナリファイルはLinuxのobjdumpで一応アセンブリに変換できる。今回の場合だと`objdump warm -S`。

`command not found`といわれる場合は`apt install binutils`で入れられる。

[hex editor](https://marketplace.visualstudio.com/items?itemName=ms-vscode.hexeditor)とかでいろいろ見てみたい

- keyword
  - [file](https://atmarkit.itmedia.co.jp/ait/articles/1605/10/news018.html)(Linuxコマンド)
