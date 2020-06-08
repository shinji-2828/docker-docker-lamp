# docker-docker-lamp
## 動作確認手順

### 起動

~~~
# docker-compose up -d
# docker-compose ps
~~~
statusがUPになっていることを確認する

#### apache
http://localhost:80にアクセスし「Hello World!!」が表示される

#### php
http://localhost:80/phpinfo.phpにアクセスし「phpinfo」が表示される

#### mysql
コンテナでbash実行
~~~
# docker exec -it docker-lamp_mysql_1 bash
~~~

docker-compose.ymlで設定したパスワードでmysqlログインする

##### バージョン確認
~~~
# mysql> select version();
~~~
