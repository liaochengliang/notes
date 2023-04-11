# how to use git book

## 1.install(ubuntu 18)

```shell
wget https://nodejs.org/download/release/v10.24.1/node-v10.24.1-linux-x64.tar.xz

sudo tar -xf node-v10.24.1-linux-x64.tar.xz -C /usr/local/

sudo apt install npm

# 切换为使用国内速度较快的淘宝镜像
sudo npm config set registry=http://registry.npm.taobao.org -g

sudo npm install gitbook-cli -g

sudo ln -s /usr/local/node-v10.24.1-linux-x64/bin/node /usr/local/bin/node

sudo ln -s /usr/local/node-v10.24.1-linux-x64/bin/npm /usr/local/bin/npm

node -v && npm -v

gitbook init book

sed -i 's@confirm: true@confirm: false@g' ~/.gitbook/versions/3.2.3/lib/output/website/copyPluginAssets.js

gitbook serve --port=8081

```

## 2.look

<http://localhost:8081>
