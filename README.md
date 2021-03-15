# docker-compose-aarch64
这是新手刚编译的 docker-compose-aarch64一些心得说明,大佬请无视

一.首先本人编译的版本是 docker-compose version 1.27.3, build 4092ae5d

二.编译后的二次编译需要的文件都在上传得文件里

三.编译前准备:

    首先确保目录存在

     mkdir /usr/local/src/docker-compose-aarch64
  
     cd /usr/local/src/docker-compose-aarch64
  
     将下载的三个文件都放在 /usr/local/src/docker-compose-aarch64 这个目录里
  
     接下来要进行本机编译:
  
     docker build . -t docker-compose-aarch64-builder
  
     静等编译完成
     
     docker run --rm -it docker-compose-aarch64-builder bash
     
     find / -name "docker-compose-Linux-aarch64"
     
     /build/dockercompose/docker-compose-Linux-aarch64
     
     接下来可以使用ls命令查看编译环境里面的文件
     
     cd /build/dockercompose
     
     ./docker-compose-Linux-aarch64 --version
     
     可以看到docker-compose 的版本号
     
     docker cp 容器id:/build/dockercompose/docker-compose-Linux-aarch64 /opt `后面就是你将镜像保存到哪个目录`
     
     
     
  镜像细节
  
  ID	sha256:b89d5eabd3a049dd24a24f9bf04942130946c53351cc512336bc9284138233c2  
  
  Parent	sha256:edbe3449410027f06d4f7d5a3dc315d414157b989a0e11fbffdd791dfdf11d1c
  
  尺寸	962.8 MB
  
  创建	2021-03-15 19:31:10
  
  构建	Docker 19.03.13 on linux, arm64
