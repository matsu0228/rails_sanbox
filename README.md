# rails_sanbox

try tutorial - https://railstutorial.jp/chapters/beginning?version=6.0#cha-beginning

## versions

```
# rbenv
$ rbenv version
3.1.2

# ruby
$ rbenv versions
  system
* 3.1.2

rails7.0.2
mysql8.0
```


## setup

```
$ docker-compose up -d

# 再ビルドも含むとき
$ docker-compose up -d --build

$ docker ps
       Name                     Command               State                          Ports                       
-----------------------------------------------------------------------------------------------------------------
rails_sanbox_db_1    docker-entrypoint.sh --inn ...   Up      0.0.0.0:3306->3306/tcp,:::3306->3306/tcp, 33060/tcp
rails_sanbox_web_1   entrypoint.sh bash -c rm - ...   Up      0.0.0.0:3000->3000/tcp,:::3000->3000/tcp 
```


then, open `http://localhost:3000` with browser.

**view logs**

```
$ docker-compose logs web 
```

**view db**

```
$ docker-compose run db bash

mysql -h localhost -u root -p**set password here**
```

## railsコマンド

- webコンテナに向けて実行する

```
# 例
docker-compose run web rails generate scaffold **
```

## 開発環境


- local ruby + rvenv - https://github.com/rbenv/rbenv#installation
- vscode - https://zenn.dev/nnt/articles/f487e07dd744d0
   - rubocop + solargraph - https://zenn.dev/massu_devix/articles/e400308d55011d