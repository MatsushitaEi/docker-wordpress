# docker-wordpress
wordpress環境をdockerで構築するための雛形

## ディレクトリ構成
docker-compose.ymlと同一フォルダに「certs」ディレクトリと「wordpress」ディレクトリを作成しておく

<pre>
.
├── certs
├── docker-compose.yml
└── wordpress
</pre>

## dockerの立ち上げ方
以下のコマンドを順番に実行
<pre>
cd docker-compose.ymlがあるディレクトリ
docker-compose up -d
</pre>

うまく立ち上がっていれば、http://IPアドレス でwordpress管理サイトにアクセスできるはずです。

※ドメイン取得が完了するまでは、docker-compose.ymlの「https-portal」コンテナは起動できないので、20-33行目は削除して利用してください。
