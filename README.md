# Dockerメモ

## コンテナをビルド
```
$ docker image build -t flask .
```

## コンテナイメージを確認
```
$ docker image ls
```

## コンテナを起動する
```
$ docker run -p 5000:80 -v ${PWD}/app:/app -d flask
```
(他のポート番号と被っている場合は`$ ~ 5000:80 ~`部分を`5001`などよしなに変更)

## コンテナの起動を確認する
```
$ docker container ls
```
停止しているものも出力させる場合は
```
$ docker container ls -a
```

## 設定したポートにアクセスする
↑の設定なら https://localhost:5000   

<hr>

## コンテナを停止する
```
$ docker stop [コンテナID]
```
(コンテナIDは `$ docker container ls` で出力できる)

<hr>

## コンテナを再起動する
```
$ docker start [コンテナID]
```
(コンテナIDは `$ docker container ls` で出力できる（２回目）)