# 后台管理平台 Node 部分 

项目采用 TypeScript + Koa 为主要技术栈，运行在[轻服务云工程](https://qingfuwu.cn/docs/cloud-project/quickstart.html)中。


## 本地安装

```sh
pnpm install
```

## 本地开发项目

```sh
pnpm dev 
// 或 inspirecloud dev
```

然后访问 http://127.0.0.1:3000

## 上传至云端

```sh
pnpm deploy
// inspirecloud deploy
```

本地上传云端需要注册轻服务账号并申请服务，然后在项目根目录下生成 `.inspirecloud.service.conf` 文件并注明 service id，例如

```conf
version=2.0

; 你的 service id
service-id=******
```

## 项目目录

```sh
project
  |- node_modules    # 该项目的依赖项的安装目录
  |- public          # 静态资源目录
  |- src             # 包含主要逻辑文件的目录，为 Koa 的工程文件
      |- controllers   # controller 是业务入口
      |- models        # model 负责数据操作
      |- routes        # route 是路由定义
      |- services      # service 是业务定义
      |- app.js        # app 是 Koa 实例定义
  |- index.js        # 云工程的入口文件
  |- inspirecloud.json  # 轻服务云工程配置文件
  |- package.json    # npm 的通用配置文件
  |- .gitignore      # Git 管理时标识忽略内容的文件
```


