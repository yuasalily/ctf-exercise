# 概要
## これは何
ctf練習

# 使っているツール
## Burp Suite

### 初期設定
- [公式サイト](https://portswigger.net/burp/communitydownload)からダウンロードしてインストールして起動([参考](https://security-blog-it.com/16472/))
- ブラウザのプロキシを設定。chromeなら[SwitchySharp](https://chrome.google.com/webstore/detail/proxy-switchysharp/dpplabbmogkhghncfbfdeeokoefdjegm?hl=ja)を使うと切り替えが楽。([参考](https://taiyakon.com/2018/05/burp-suite-macosgoogle-chrome.html))

以下はhttpsで通信する際に必要な設定。
- Burp Suite起動後、localhost:8080に接続して証明書を入手([参考](https://www.leon-tec.co.jp/blog/diary/10174/#fourth))。
- chromeに証明書をimport
  - chromeの設定を開く
  - プライバシーとセキュリティを開く
  - セキュリティを開く
  - 証明書の管理を開く
  - 信頼されたルート証明機関のタブを開き、インポートを押して証明書をインポートする。
- [SwitchySharp](https://chrome.google.com/webstore/detail/proxy-switchysharp/dpplabbmogkhghncfbfdeeokoefdjegm?hl=ja)を使っている場合はHTTPS ProxyにHTTP Proxyと同じものを追加する。
 
インポートした証明書を削除する方法
- 信頼されたルート証明機関のタブを開く
- PortSwigger CAを探し、削除を選択する
- [SwitchySharp](https://chrome.google.com/webstore/detail/proxy-switchysharp/dpplabbmogkhghncfbfdeeokoefdjegm?hl=ja)を使ってる場合はHTTPS Proxyを空白にするのを忘れない

### 使い方
[参考](https://persol-tech-s.co.jp/corporate/security/article.html?id=10)

### メモ
- windowsの場合`certmgr.msc`でも証明書の管理ができる。

## WireShark
