# 基于 Hexo + GitHub Pages搭建博客

hexo是一个简洁高效的博客框架，可移步[hexo官网](https://hexo.io/)详细了解。

GitHub Pages是GitHub的网站托管服务，可以将仓库变成一个静态资源服务器。

基于上述两者即可白嫖一个自己的网站。

## 搭建方法
* 1、创建站点目录。在github上创建一个与你账号同名的repositories，即yourname.github.io

* 2、安装hexo
```
$ npm install -g hexo-cli
```

* 3、初始化站点目录，hexo在指定目录中创建源文件，并通过npm安装相关依赖库。
```
$ mkdir <folder>
$ hexo init <folder>
$ cd <folder>
$ npm install
```

* 4、生成博客，本地预览。
```
$ hexo generate
$ hexo server
```

* 5、部署到GithubPages。hexo提供了一种便捷方式，通过修改_config.yml配置，即可通过命令行将文件部署到对应仓库的指定分支。
```
deploy:
    type: git
    repo: git@github.com:yourname/youname.github.io.git
    branch: blog
```

* 6、安装插件。
```
$ npm install hexo-deployer-git --save
```

* 7、发布本地博客到远程仓库。
```
$ hexo deploy
```

* 8、配置githubPages。上述deploy配置可见我将代码上传到了blog分支上了（当然你可以传到master上），在GitHub的该仓库的settings-Pages中将source更改为blog分支，save后在地址栏输入yourname.github.io即可访问到你的博客啦~
