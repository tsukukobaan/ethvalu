# BLOW ethvalu
## リポジトリ概要
valu的なものを、ちゃんとトークン発行してやろうというものです。BLOWと呼びます

## QuickStart
* 仮想環境を立ち上げる

    ```
    . bin/activate
    ```
    
* pip で必要パッケージのインストール

    ```
    pip install -r requirements.txt
    ```
* src/ディレクトリに移動 _ソースはsrcに入っている_

    ```
    cd src
    ```
* django のインストールを確認

    ```
    pip freeze` or `django-admin.py version
    ```
    1.10.3をインストールしている
* DBを作成

    ```
    python manage.py makemigrations
    python manage.py migrate
    ```
    
* admin用のsuperuserを作成

    ```
    python manage.py createsuperuser
    ```
* 起動

    ```
    python manage.py runserver
    ```

## Makefileでコマンド管理しています
* Migrationファイルを作る

    ```
    python manage.py makemigration
    ```
    
    は

    
    make migrations
    

* Migrateする

    ```
    python manage.py migrate
    ```

    は
    
    
    make migrate
    
    
* サーバーを始動する

    ```
    python manage.py runserver
    ```
    
    は
    
    
    make run
    
    
    ※　別ターミナルでgeth用サーバーを立てること
    
    
    geth --rpc --rpcapi "personal,eth" --dev --networkid 123 console
    

