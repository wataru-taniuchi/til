# `gem install`で`/usr/bin`が`Operation not permitted`になる

## SIP（System Integrity Protection）

OS X 10.11 El Capitanから追加されたOS自体のセキュリティ機能  
以下のディレクトリはroot権限でも書き込みができない
* /bin
* /sbin
* /System

## 回避方法
`/usr/local/bin`にインストール先を変更する
```
gem install bundler -n /usr/local/bin
```