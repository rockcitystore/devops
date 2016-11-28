>#registry

本机器用于搭建docker私有仓库

####安装&运行
```
 install docker
 sudo docker run -d -p 5000:5000 -v /opt/:/var/lib/registry registry
```

`http://192.168.33.211:5000/v2/_catalog` 可以列出已有镜像



####其他机器拉取私有镜像时

需要如下操作
```
#centos7.2;
vi /usr/lib/systemd/system/docker.service

#修改
ExecStart=/usr/bin/dockerd --insecure-registry 192.168.33.211:5000

#重启服务
#service docker restart
systemctl daemon-reload

#https://my.oschina.net/u/1538135/blog/672364
```