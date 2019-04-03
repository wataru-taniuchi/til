# 今更docker環境構築
## dockerとは
> コンテナ型仮想環境

ホストOS上に仮想環境領域を作成する。  
FYI: [仮想環境の種類](https://qiita.com/9en/items/f4eab2f61485a9f3885a)

## 構築手順 for Mac
#### アプリケーションのインストール
1. [dockerhub](https://hub.docker.com/editions/community/docker-ce-desktop-mac)からダウンロード
2. `Docker.dmg` を実行してインストール
3. 確認コマンド 
```
$ docker -v
Docker version 18.09.2, build 6247962
```

#### イメージのダウンロード
1. dockerhubから目的のイメージをpull
```
$ docker pull centos:7
```
2. イメージからコンテナを作成
```
$ docker run -it --name centos7 -d centos:7
```
※ ２回目以降の起動と停止は 
```
$ docker start centos7
$ docker stop centos7
```
1. コンテナに接続
```
$ docker exec -it centos7 bash
```
4. 確認
```
$ cat /etc/redhat-release
CentOS Linux release 7.6.1810 (Core) 
```
