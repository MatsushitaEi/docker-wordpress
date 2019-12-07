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
dockerコマンドがサーバー上に入っていない場合、以下の記事等を参考に事前にインストールしておいてください。
https://qiita.com/youtangai/items/ff67ceff5497a0e0b1af

以下のコマンドを順番に実行
<pre>
cd docker-compose.ymlがあるディレクトリ
docker-compose up -d
</pre>

うまく立ち上がっていれば、http://IPアドレス でwordpress管理サイトにアクセスできるはずです。

※ドメイン取得が完了するまでは、docker-compose.ymlの「https-portal」コンテナは起動できないので、20-33行目は削除して利用してください。
