# 使用minio部署静态网站

因已有minio环境，所以本文档是使用minio发布。


## 创建bucket

1. 创建一个名字为`html`的bucket。
2. 设置自定义权限，公开读。
3. 在`html`bucket中创建目录`writerside.cn`,建议用网站域名作为路径前缀，网站较多时，好区分。
4. 通过minio console 管理界面，上传Writerside构建的html文件。
5. 已经可以通过minio服务访问文档了，可以继续使用nginx配置专用域名。



## 配置Nginx

域名`writerside.cn`解析到minio服务。

配置文件如下
```
server {
    listen       80;
    listen       443  ssl;
    server_name  writerside.cn www.writerside.cn;

    #强制访问主域名
    if ( $host != 'writerside.cn' ) {
        rewrite ^(.*)$ https://writerside.cn$1 permanent;
    }
    #强制访问HTTPS
    if ( $scheme = 'http') {
        rewrite ^(.*)$ https://$host$1 permanent;
    }

    #SSL配置这里不提供
    ...
    
    location / {
        proxy_pass http://minio.intranet.mosong.cc/html/writerside.cn/;
    }
}
```

Nginx配置里的`proxy_pass`地址，`html`是bucket名字，`writerside.cn`是路径前缀。