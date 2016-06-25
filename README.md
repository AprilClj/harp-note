## Harp　简介(introduction)
 Harp 是一个基于 Node.js 平台的静态 Web 服务器，
 内置流行的预处理器，支持把 Jade, Markdown, EJS, Less, Stylus, Sass, and CoffeeScript 
 转换为 HTML、CSS、JavaScript，不需要进行任何的配置。

## Harp　依赖(denpendency)

Harp依赖于NodeJS和NPM包管理器（node.js安装自带NPM）。你可以从官网下载最新版的NodeJS。
一旦安装了node.js和NPM，就可以使用NPM安装Harp。

## Harp 安装(install)

- OS X 系统上　 Applications → Utilities → Terminal.
              (应用程序　　-->　公用　-->终端　)
- Linux　　　　　   Applications → Utilities → Terminal.
              (应用程序　-->　终端　)
- 在终端输入　sudo npm install -g harp (当登录用户有权限时　可以省略sudo　)

## Harp 更新(update)
直接运行 npm install -g harp 
若出现错误　使用如下命令

- npm uninstall -g harp
- npm cache clear  清理缓存
- npm install -g harp

## Harp 初始化(init)

harp init [path]

path 该文件夹路径用来存放项目，项目初始化之前，文件夹必须为空，否则无法创建任何文件

eg:进入一个空文件夹　在当前目录下　打开终端　运行　harp init

项目默认的结构如下

文件夹名称/

  |- _layout.jade
  
  |- 404.jade
  
  |- index.jade
  
  +- main.less

eg:直接运行 harp init myproject

生成目录如下

myproject/
  |- _layout.jade
  |- 404.jade
  |- index.jade
  +- main.less

默认的应用使用jade模板来映射HTML,你也可以使用更为常见的EJS.

### 使用一个模板(--boilerplate)

1.默认的harp 模板应用

harp init myproject --boilerplate docs

或者

harp init myproject --b docs

2.制定某个用户下的特定模板

harp init myproject --boilerplate kennethormandy/hb-remedy

3.用任何其他基于网页技术的项目作为模板

harp init -b phonegap/phonegap-start

harp server www

##Harp 服务(Server)

harp server [options] [path]  启用运行某一个应用服务

Options 

- port -(数值类型)　可选项　服务器监听的端口，默认端口是9000;
- help - 显示帮助列表项

path - (字符串)　可选项　服务器监听的路径

eg: harp server ~/apps/example.com --port 3000

访问一个运行的harp 应用

- http://harpdev.io:3000
- http://127.0.0.1:3000
  
如果没有制定端口　harp应用使用　http://127.0.0.1:9000进行访问

使用端口80 每次访问不需要添加端口号便能访问

sudo harp server --port 80


# Harp(编译) compile

导出项目中的静态资源　--css html js

-harp compile [options] [projectPath] [outputPath]

eg:命令行运行下面语句

－ harp init mobileapp
－harp compile mobileapp

生成如下目录

  mobileapp/
  
    +- www/
    
      |- index.html
      
      +- main.css
 

harp compile ~/apps/example ~/Desktop/backup
将apps下的example项目 编译到Desktop下的backup目录中





