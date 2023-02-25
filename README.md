## docker
cd .docker
docker-compose up -d
docker-compose exec scrapy bash

## Scrapy コマンド

### バージョン確認
scrapy version

### プロジェクト作成
scrapy startproject (project_name)

### spider 作成
cd (project_name)
scrapy genspider blog https://pointsandlines.jp/

## （Python）

### Python バージョン確認
python3 -V

## pip バージョン確認
pip --version

## ライブラリ追加
/var/requirements.txt へライブラリ名記載

pip install -r ./requirements.txt

## インストール済みライブラリ確認
pip list