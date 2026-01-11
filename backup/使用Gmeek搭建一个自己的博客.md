# 1. 什么是Gmeek
[Gmeek](https://github.com/Meekdai/Gmeek) 一个博客框架，超轻量级个人博客模板，完全基于`Github Pages` 、 `Github Issues` 和 `Github Actions`，可以称作`All in Github`。不需要本地部署，从搭建到写作，只需要18秒，2步搭建好博客，第3步就是写作。
# 2. 搭建Gmeek
## 2.1 注册Github
这个...应该不用教了吧
打开[Github](https://github.com)注册就完事了
## 2.2 创建仓库
打开[链接](https://github.com/new?template_name=Gmeek-template&template_owner=Meekdai)
推荐输入`你的Github用户名.github.io`，这样会有一个免费域名
点击`Create repository`
## 2.3 启用Pages
打开`Settings`，点击`Pages`，选择`Github Actions`
这样就完成了
## 2.4 配置博客
点击`config.json`
里面会有如下内容
```json
{
    "title":"Meekdai",
    "subTitle":"童话是一种生活态度，仅此而已。",
    "avatarUrl":"https://github.githubassets.com/favicons/favicon.svg",
    "GMEEK_VERSION":"last"
}
```
修改一次，比如我的
```json
{
    "title":"TR114514の小窝",
    "subTitle":"114514。",
    "avatarUrl":"https://github.githubassets.com/favicons/favicon.svg",
    "GMEEK_VERSION":"last"
}
```
修改完毕后保存即可
## 2.5 开始写作
直接在`Issues`里面写文章即可，记得带`Labels`
## 官方教程
见[Gmeek快速上手](https://blog.meekdai.com/post/Gmeek-kuai-su-shang-shou.html)
# 3. b站视频教程
`Gmeek-html<iframe src="//player.bilibili.com/player.html?isOutside=true&aid=1305790042&bvid=BV1GM4m1m7ZD&cid=1588230883&p=1" scrolling="no" border="0" frameborder="no" framespacing="0" width="100%" height="460px allowfullscreen="true"></iframe>`