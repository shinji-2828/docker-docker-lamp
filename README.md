# docker-docker-lamp
## 動作確認手順

### 起動

~~~
# docker-compose up -d
# docker-compose ps
~~~
statusがUPになっていることを確認する

#### apache
http://localhost:80 にアクセスし「Hello World!!」が表示される

#### php
http://localhost:80/phpinfo.php にアクセスし「phpinfo」が表示される

#### mysql
コンテナでbash実行
~~~
# docker exec -it docker-lamp_mysql_1 bash
~~~

docker-compose.ymlで設定したパスワードでmysqlログインする

#### phpmyadmin
http://localhost:8080 にアクセスし「ログイン画面」が表示される

docker-compose.ymlで設定したパスワードでmysqlログインする

##### バージョン確認
~~~
# mysql> select version();
~~~

### tips
VMの場合はIPを調べる
~~~
# docker-machine ls
~~~

### 停止、終了

~~~
docker-compose stop
docker-compose down

docker rm [id or name]
docker rmi [id or name]
~~~
