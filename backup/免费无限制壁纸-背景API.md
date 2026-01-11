# 1. 调用

直接上链接
```http
# 下面这个是PC，即电脑版的
GET https://g-bg-api.traveler.dpdns.org/h
# 下面这个是手机版的
GET https://g-bg-api.traveler.dpdns.org/v
```
# 2. 搭建教程
## 2.1 部署到Cloudflare Pages
打开 [TR114514-Coder/bg-api](https://github.com/TR114514-Coder/bg-api)
`Fork`一份到自己的账号下
然后`git clone`下来
把你的图片放到`oriImg`里面
注意，`h`是横向的，也就是电脑版，`v`是竖向的，也就是手机版
然后`python gen_img.py`
他就会把图片弄到`dist`文件夹里面
接下来，你可以`git push`上去，也可以压缩`dist`文件夹
如果你是`push`上去的，请你在`Cloudflare`新建一个`Pages`
然后链接你的`Git存储库`也就是你`Fork`的库
如果是压缩`dist`文件夹的话，就把压缩包上传到`Cloudflare Pages`
接下来把构建目录设置为`dist`
最后绑定一个`自定义域名`即可
## 2.2 设置规则
点击你托管的域名
在左侧点击`规则`，然后点击`概述`
新建一个`URL重写`规则
`规则名字`随便填
在`如果传入请求匹配…`中选择`自定义筛选表达式`
`当传入请求匹配时...`按照下面这样子填
```text
字段|运算符|值
主机名|等于|这里写你你的`Pages`绑定的域名地址
And
URI 路径|等于|/h
Or
URI 路径|等于|/v
```
`表达式预览`是这样的
```text
(http.host eq "你Pages绑定的域名地址" and http.request.uri.path eq "/h") or (http.request.uri.path eq "/v")
# 这里贴上我的表达式
(http.host eq "g-bg-api.traveler.dpdns.org" and http.request.uri.path eq "/h") or (http.request.uri.path eq "/v")
```
在下面`路径`这里面选`重写到`
然后选择`Dynamic`
输入下面这个
```text
concat(http.request.uri.path, "/", substring(uuidv4(cf.random_seed), 0, 3), ".jpg")
```
完整的配置图如下
`Gmeek-html<img src="https://img.traveler.dpdns.org/v2/vaJ3Uor.png">`
然后点击`保存`
接下来就弄好了
## 访问地址
```http
# 电脑版
GET https://你的域名/h
# 手机版
GET https://你的域名/v
```