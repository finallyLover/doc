# #安装

1、新建文件夹PhotoPrism 

```
mkdir PhotoPrism
cd  PhotoPrism
```

2、创建 docker-compose-photoPrism.yml文件 

```
vi docker-compose-photoPrism.yml
```

3、[点我](file/docker-compose-photoPrism.yml)获取文件内容

4、执行启动命令

```
docker-compose -f docker-compose-photoPrism.yml up -d
```

5、访问首页地址

备注：

1、账号密码在配置文件地址

2、需要安装mariadb 创建名字为photoprism的数据库

http://ip:2342

![image-20250114214227687](G:\project\my-project\doc\杂项\PhotoPrism\images\image-20250114214227687.png)