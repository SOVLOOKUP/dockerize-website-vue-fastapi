# **Vue+FastAPI+mongodb Dockerize网站部署**

## 简介

提供了一个快速部署模板，能够进行快速建站。使用了Nginx+Vue+FastAPI+mongodb。


## 前序准备

1. 部署前安装Docker

2. 将vue项目编译为静态文件

## 部署

```bash
# 克隆项目
git clone https://github.com/sovlookup/dockerize-website-vue-fastapi

# 进入项目目录
cd dockerize-website

# 进入静态文件目录
cd nginx/web/ # 将你编译后的网站前端放置于此

# 进入后端文件目录
cd api/app # 将你的网站后端放置于此

# 修改docker-compose.yml line20
VUE_APP_BASE_API=http://这里写你的域名/api/

# 回到根目录 启动
docker-compose -f docker-compose.yml up --build
```

网站搭建完毕 浏览器访问 http://localhost



## 其它

```
# URL规范
VUE_APP_BASE_API代理到后端的/

因此Vue项目中只需要指定baseurl为VUE_APP_BASE_API，API地址完全按照文档即可
（真实url = baseurl + 相对url）

# 例如
前端：在 '/test' post了 'aaa'
后端：在 '/test' 接收到 'aaa'

```

## License

[MIT](https://magicdawn.mit-license.org/)

Copyright (c) 2020-present XiaFan
