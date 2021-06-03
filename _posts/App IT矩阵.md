# 构建的服务

环境需要

nodejs, java, python

mongo, 

nginx


java云端加密
本地bash脚本打包dex

## python写的那个flask 支付程序

不可以直接对外暴露，传输页面过程有问题，所以用nginx套一层

3003反射3001的



## 自己平时跑的download程序

8081

## ws

ws 3004 

http 3005



## http

8081

# nginx写法


```nginx
server {
    listen 3003;
    index index.html index.htm;
    proxy_set_header X-Forwarded-For $remote_addr;
    location / {
          proxy_pass http://localhost:3001;
          proxy_set_header Host $host:$server_port;
    }
}
```
