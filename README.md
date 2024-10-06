# dockerDebian
## apt-get installするパッケージ
```
wget - ファイルをダウンロードするためのユーティリティ
build-essential - コンパイルに必要なツールセット
libffi-dev - C言語で書かれたライブラリを開発するためのパッケージ
libssl-dev - SSL/TLS通信のためのライブラリ
zlib1g-dev - 圧縮および解凍ライブラリ
libbz2-dev - BZIP2圧縮のためのライブラリ
libreadline-dev - ユーザー入力のためのライブラリ
libsqlite3-dev - SQLiteデータベースのライブラリ
curl - URLからデータを取得するコマンド
llvm - コンパイラおよびツールチェーン
libncurses5-dev - ターミナルUIアプリケーションを開発するためのライブラリ
libncursesw5-dev - ワイド文字対応のncursesライブラリ
xz-utils - LZMAデータ圧縮/伸長ツール
tk-dev - Tcl/Tkのライブラリとヘッダーファイル
liblzma-dev - XZ形式のライブラリ
git - バージョン管理ツールGit
ca-certificates - 証明書関連のパッケージ
openssh-client - SSHクライアントツール
```

docker-compose exec myapp bash
mysql -h mysql -u root -D django-db -proot
cd app/python/Django/djangotodo/
python3.11 manage.py makemigrations
python3.11 manage.py migrate
python3.11 manage.py runserver 0.0.0.0:8000