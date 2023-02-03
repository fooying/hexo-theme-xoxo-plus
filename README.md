# hexo-theme-xoxo-plus
A hexo them modification based on [hexo-theme-xoxo](https://github.com/KevinOfNeu/hexo-theme-xoxo)

[Demo](https://www.fooying.com)

### 新增应用类型
* 友情链接 links
* 动态 activity
* 项目 project
* paper paper

需要在站点根目录的source目录下建立对应的目录并且添加index.md，如:
```
 ---
   title: Activity
    date: 2019-03-01 13:45:13
    type: "activity"
 ---
```

具体配置需要在模板_config.yml 配置，具体可见下方说明

### 新增开关及调整
1. 百度链接提供JS自动推送
```
# 模板_config.yml中配置
baidu_url_js_push: false
```
2. UI的微调，主要为header部分
3. 文章页尾部二维码关注增加开关并可配置
```
# 模板_config.yml中配置
share:
    show: false #展示开关
    img: #图片地址
    img_alt: #图片alt
    tip_text: #图片底部提示文字
```
4、增加logo配置，区分logo和favicon配置
```
# 模板_config.yml中配置
favicon: footer-logo.png # favicon配置
logo: # logo配置
```
5、新增gitalk/giscus评论支持
```
# 模板_config.yml中配置
# disqus同时配置的情况下，优先选择模板中配置的评论系统
# clientID、clientSecret的生成请访问申请 https://github.com/settings/applications/new
# giscus 配置参考 https://giscus.app/zh-CN
comment_extend:
    gitalk:
        enable: true
        owner: Github username
        repo: issue repo name
        admin: github username
        clientID: xxx
        clientSecret: xxx
   giscus:
        enable: false
        repo: data-repo
        repoId: data-repo-id
        dataCategoryId: data-category-id 
```

### _config.yml 配置说明
相关示例可参考项目中_config.yml文件
1、配置友情链接
```
links:
   name1: url1
   name2: url2
   ...
```

2、配置项目
```
projects:
  project name1:
    url:  url1
    descript: project descript
  project name2:
    url:  url2
    descript: project descript
  ...
```

3、配置活动
```
activitys:
  title1:
    date: 2018-09-10 # 时间，只能YYYY-MM-DD
    url: url
    type: 采访 # 类型，可自定义
  ...
```

4、配置paper
```
papers:
  titile: url
  ...
```


### 错误处理
1、readingTime is not defined

安装插件hexo-reading-time
