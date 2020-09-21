# tcprstat 0.3.1 with docker running demo


## tcprstat build

* source code

https://github.com/y123456yz/tcprstat

* build

> with centos 7 

```code
git clone https://github.com/y123456yz/tcprstat.git
yum -y install bison yacc flex  glibc-static  libcap-devel
./configure
make &&  make  install
```

## running demo

> with  tomcat app

* start demo service

```code
docker-compose up -d  tcprstat-demo
```

* running  tcprstat test lagency


```code
docker-compose exec tcprstat-demo sh
cd  /opt/tcprstat  && ./tcprstat -p 8080 -t 1  -n 0
```
