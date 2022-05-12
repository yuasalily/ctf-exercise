### Description
このファイルを開きたいが拡張子がないので、どのような種類のファイルで、どのアプリケーションで開けば良いかわからない。
どうにかして、この拡張子がないこのファイルの種類を特定し、どのアプリケーションで開くか調べてくれ。

### Writeup
ダウンロードしたファイルをwordで開くとflagが得られる。


### memo
ファイルの種類はLinuxの`file`コマンドで確認できる。今回の場合だと

`file -i exec_me`

とすれば

`open_me: application/msword; charset=binary`

と出てくる。これで実行可能なファイルだとわかる。ファイル形式を判定するものだと[こんなサイト](http://ixtlilton.net/cgi/FileMimeChk.cgi)もある。

- keyword
  - [file](https://atmarkit.itmedia.co.jp/ait/articles/1605/10/news018.html)(Linuxコマンド)
  
