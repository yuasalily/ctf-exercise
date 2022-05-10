### Description
JPEGという画像ファイルのフォーマットでは、撮影時の日時、使われたカメラ、位置情報など様々な情報(Exif情報)が付加されることがあるらしい。
この情報から、写真に写っている川の名前を特定して欲しい。
### Writeup
exif情報を読み取って場所を特定する。exif情報を読み取るにはexiftoolを使うか、オンラインであれば[このようなサイト](http://exif-viewer.com/)がある。

場所の特定に必要な項目は
- GPSLatitude	31/1, 35/1, 69/25
- GPSLongitude	130/1, 32/1, 64659/1250
である。
これはそれぞれ度，分，秒で表されているので変換する必要がある（[参考](https://support.google.com/maps/answer/18539?hl=ja&co=GENIE.Platform%3DDesktop)）。

変換方法
```
x = 31/1 + 35/1/60 + 69/25/3600
y = 130/1 + 32/1/60 + 64659/1250/3600
print(x)
print(y)
```
この結果を[googlemapで検索](https://support.google.com/maps/answer/18539?hl=ja&co=GENIE.Platform%3DDesktop)すればflagに必要な川の名前を得られる。

主要なSNSではexif情報は自動で消されるらしい。

- keyword
  - [exif](https://ja.wikipedia.org/wiki/Exchangeable_image_file_format)
