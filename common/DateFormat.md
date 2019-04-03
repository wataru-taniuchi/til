# 年末年始日付の取得で起きたこと
 
## TL;DR
日付をフォーマット指定して出力したい場合は 西暦の部分は`yyyy` と小文字で指定する


## 何が起こったか
プログラム内で`YYYY/MM/dd`の形式で指定した日付を取得する処理があった。  
`2018/12/30`を指定しているはずなのに出力される値が`2019/12/30`で出力されていた。

## 原因
元になった`YYYY/MM/dd`の形式は[ISO 8601](https://ja.wikipedia.org/wiki/ISO_8601)では、`木曜日を含む週をその年の第1週とする`という決まりがある。
2018/12/30はカレンダーだと日曜日で、木曜日は2019/01/03になるため出力が2019/12/30になってしまう。

## 対処
どの言語でもこれに対処するために小文字の`yyyy`が指定できるようになっている。（どこが策定しているかは出てこなかった）
そのため`yyyy/MM/dd`と指定させることによって、2018/12/30がちゃんと2018/12/30として出力されるようになった。

## 余談
2016/12/31は土曜日なのでちゃんと出力される。

## 参考
https://qiita.com/kazuhiro4949/items/d8fc27c0a0b6d88f1a80