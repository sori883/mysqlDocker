# mysqlDocker
DockerでMySQL
- MySQL5.7
- phpMyAdmin

# 使用法
## volumes
#### Windowsのボリューム記述
どこか適当なディレクトリに入れる
docker > setting > Shared Drivesで使うドライブにチェックが入っている状態にしとく  
（WidowsにMSアカウントでログインしてるとチェック出来ない？のでローカルアカウントでやる）

#### MACのボリューム記述
どこか適当なディレクトリに入れる  
docker-compose.ymlのvolumesを以下の通り編集
```
volumes:
    - ./db/data:/var/lib/mysql
    - ./db/my.cnf:/etc/mysql/conf.d/my.cnf
```

あとは下記の通り  
```
$ cd mysqlDocker
$ docker-compose up -d
```

起動したらブラウザで`localhost:8080`にアクセスして確認。  
![screenshot 4](https://user-images.githubusercontent.com/37400002/60772162-5731ea00-a12d-11e9-8476-ec08b6a31fa2.jpg)  

一応、MySQL Workbenchでも入れます。。。。  
![screenshot 5](https://user-images.githubusercontent.com/37400002/60772214-2bfbca80-a12e-11e9-8762-62a7a7fe5140.jpg)  


