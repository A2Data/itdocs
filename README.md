# itdocs

## Hexo 主题 Docs

一个简洁的主题，主要功能是 “树状导航” + “树状目录” + "标题导航"，可选配“评论”和“阅读量”功能，增加了留言，公告。Twikoo留言功能。



一直比较喜欢`vuepress`  以及`gitbook` 那样的样式的,奈何 很多都找不到， 所以自己魔改了一些。效果如下

![](https://7.dusays.com/2021/05/30/a73a3c547c88c.png)



支持评论，个人二维码等。

![](https://7.dusays.com/2021/05/30/9ca0c5ae41a68.png)



## 使用说明

1、首先在`source`·下 建立index 文件夹，再在其中建立
`index.md`



2、部署插件

```bash
npm install hexo-deployer-git --save

# 可以多个
deploy:
  - type: git
    repo: git@118.190.107.96:/home/git/blog.git       #此处的SERVER需改为你自己服务器的ip
    branch: master                            #这里填写分支
    message:                                  #提交的信息
```



3、搜索插件

```shell
hexo-generator-search

hexo-generator-searchdb


# 配置
search:
  path: search.xml
  field: post
  content: true
```



4、加密插件

```bash
hexo-blog-encrypt

# 配置
encrypt: # hexo-blog-encrypt
  abstract: 这里有一些加密的东西，需要密码才能继续读取。
  message: 你好，这篇文章需要密码
  tags:
    - {name: plan, password: datascience}
  wrong_pass_message: 亲，这是一个无效的密码。请检查后再试。
  wrong_hash_message: 亲，这些解密的内容无法验证，但你仍然可以看一看。

```



5、永久链接

```bash
npm install hexo-abbrlink --save

# 永久链接
abbrlink:
  alg: crc32   #算法： crc16(default) and crc32
  rep: hex     #进制： dec(default) and hex
  start: 1000 # the first id, default 0
```



## 初心

![](https://7.dusays.com/2021/05/29/08238220cd7e6.jpg)





