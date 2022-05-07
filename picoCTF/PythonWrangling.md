### Description
Python scripts are invoked kind of like programs in the Terminal... Can you run this Python script using this password to get the flag?

### Writeup
usage_msgに書いてある通り下記のコマンドを実行後、pw.txtの中身を入力すればflagが得られる。
`python ende.py -d flag.txt.en`

以下のように直接pw.txtの中身をコマンドライン引数で渡してもok。

`python ende.py -d flag.txt.en 68f88f9368f88f9368f88f9368f88f93`

### memo

- keyword
  - [base64](https://ja.wikipedia.org/wiki/Base64)
  - [cryptography](https://timesaving.hatenablog.com/entry/2020/12/31/110000)


