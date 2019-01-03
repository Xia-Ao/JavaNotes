# fastDFS配合nginx 安装配置

### fastDFS安装过程
参考：https://blog.csdn.net/softwave/article/details/54017095

注意中间要将http.conf文件 复制到 /etc/fdfs下

目录：
* `/etc/fdfs` 核心配置文件
最终配置文件组成
```
-rw-r--r-- 1 root root  1458 Dec  4 08:51 client.conf   // 客户端配置文件
-rw-r--r-- 1 root root   943 Dec  4 09:49 http.conf         // http 服务，
-rw-r--r-- 1 root root 31172 Dec  4 11:10 mime.types    // fastdfs-nginx-module需要
-rw-r--r-- 1 root root  3731 Dec  4 11:59 mod_fastdfs.conf  // fastdfs-nginx-module 配置
-rw-r--r-- 1 root root  7923 Dec  4 08:58 storage.conf          // storage配置
-rw-r--r-- 1 root root   105 Dec  4 08:22 storage_ids.conf.sample // 不知道干嘛的
-rw-r--r-- 1 root root  7386 Dec  4 08:43 tracker.conf          // tracker配置
```

* `/soft/fastdfs/fastdfs.....` 安装目录
* `/home/fastdfs/`  数据存储， 日志目录


### nginx 安装目录
* `/soft/nginx/nginx-1.15.7` 安装目录
* `/usr/local/nginx/`   配置文件目录
* `/usr/local/nginx/sbin`   执行文件目录


### fastdfs-nginx-module 安装
总体来讲其实没有那么麻烦，在安装过程中 遇到了一些错误，google之后找到解决方案，其实还算比较顺利，
* `/soft/fastdfs/fastdfs-nginx-module`   安装目录

参考： https://blog.csdn.net/zgf19930504/article/details/51891713

教程里面有一个地方有问题，在修改文件 xx/fastdfs-nginx-module_v1.16/src/config时，需要修改的地方是两个， 不然在nginxmake编译的时候回报错
![](../assets.fastdfs.png)

