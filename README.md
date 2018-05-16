Pokeman
====

Requirements
----

- node
- docker

Setup
----

1. 安装依赖

```
brew install pkg-config cairo pango libpng jpeg giflib
```

2. 启动 MongoDB

```sh
docker run -d --name=pokeman-mongo -p 27017:27017 mongo:3.6
```

3. 配置环境变量

```
export POKEMAN_DATABASE_URI=mongodb://127.0.0.1:27017
export POKEMAN_DATABASE_NAME=pokeman
export POKEMAN_RTM_TOKEN=50c9387ad684f001b8156ec79b44eebb
```

4. 启动 Pokeman

```sh
node index.js
```
