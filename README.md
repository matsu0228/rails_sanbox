# rails_sanbox

## setup

```
$ docker-compose up -d

$ docker ps
       Name                     Command               State                          Ports                       
-----------------------------------------------------------------------------------------------------------------
rails_sanbox_db_1    docker-entrypoint.sh --inn ...   Up      0.0.0.0:3306->3306/tcp,:::3306->3306/tcp, 33060/tcp
rails_sanbox_web_1   entrypoint.sh bash -c rm - ...   Up      0.0.0.0:3000->3000/tcp,:::3000->3000/tcp 
```


then, open `http://localhost:3000` with browser.

## env

```
ruby3.1.1
rails7.0.2
mysql8.0
```