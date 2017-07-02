## 前言
作为一个开发者，记录平时的学习历程，撰写个人博客是一个不错的选择。
## 准备
1. github
你需要有一个自己的[github](https://github.com/)帐号，然后新建一个仓库（==new repository==），并且命名为==username.github.io==，==username==为你注册时填写的名称。
1. git
下载并安装[git](https://git-scm.com/)。
1. nodejs
下载并安装[nodejs](https://nodejs.org/)
## hexo安装及搭建
1. hexo安装
```shell
$ npm install -g hexo-cli
```
1. hexo初始化创建一个目录

```shell
$ hexo init <folder>
$ cd <folder>
$ npm install
```
初始完后，你的目录结构如下

```
.
├── _config.yml
├── package.json
├── scaffolds
├── source
|   ├── _drafts
|   └── _posts
└── themes
```
1. 新建一个页面

```shell
$ hexo new "Hello World"
```
在/source/_post里添加hello-world.md文件，之后新建的页面都将存放在此目录下。
1. 生成网站

```shell
$ hexo generate
```
此时会将/source的.md文件生成到/public中，形成网站的静态文件。
1. 启动服务

```shell
$ hexo server -p 3000
```
输入==http://localhost:3000==即可查看网站。
1. 部署到github

```shell
$ hexo deploy
```
输入==username.github.io==即可查看网站。
## 参考
[hexo](https://hexo.io/zh-cn/)官网