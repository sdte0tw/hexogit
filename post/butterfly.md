---
title: Butterfly主题配置
date: 2020-08-17
hide: true
copyright_author: sdte0tw
copyright_author_href: https://github.com/sdte0tw
copyright_url: /butterfly
copyright_info: 一些关于博客Butterfly主题的设置
categories: 
- 学习
- 网页
---
# Butterfly主题的安装

## 安装
>Git 安装
>>在 hexo 的根目录打开 Git Bash，输入
`git clone -b master https://github.com/jerryc127/hexo-theme-butterfly.git themes/butterfly`
如果想要安装比较新的 dev 分支，可以
`git clone -b dev https://github.com/jerryc127/hexo-theme-butterfly.git themes/butterfly`

>npm 安装
>>在 hexo 的根目录打开 Git Bash，输入`npm i hexo-theme-butterfly`
使用 npm 安装后的主题文件生成于目录中的 node_modules\hexo-theme-butterfly，可手动转移主题文件夹至根目录的 themes 中

## 应用
安装完成后，修改根目录的“网站配置文件”`_config.yml`，把`theme`改成`butterfly`（修改其他主题同理）
```yaml
theme: butterfly
```
>`网站配置文件`中的 theme 一定要与主题文件夹同名，否则会自动运行默认主题

## 插件
若此时运行`hexo s`无法正常生成页面，需要安装插件
```powershell
npm install hexo-renderer-pug hexo-renderer-stylus --save
```

# 主页导航菜单
修改`主题配置文件`中的`menu`
```yaml
menu:
  首页: / || fas fa-home
  时间轴: /archives/ || fas fa-archive
  标签: /tags/ || fas fa-tags
  分类: /categories/ || fas fa-folder-open
  娱乐||fas fa-list:
    - 音乐 || /music/ || fas fa-music
    - 电影 || /movies/ || fas fa-video
    - 照片 || /Gallery/ || fas fa-images
  链接: /link/ || fas fa-link
  关于: /about/ || fas fa-heart
```
>格式为：按钮名称: /链接/ | | 图标名 [font-awesome](https://fontawesome.com/icons?from=io) 

# Banner

## 主页banner
在`主题配置文件`中修改`index_img: 图片地址`
归档页`archives页`的banner可修改`主题配置文件`中的`archive_img`
>若图片地址留空则自动变为纯色

## 博文页banner
在`博文 Front-matter`中设置`top_img: 图片地址`即可，若未设置会使用博文封面`cover`的图片地址，若未设置封面则会使用`default_top_img`中的图片

# 博文外部相关

## 博文置顶
需要安装插件 [hexo-generator-index-pin-top](https://github.com/netcan/hexo-generator-index-pin-top)
先卸载 hexo-generator-index，然后在`博文 Front-matter`中添加`top: true`属性来把这篇博文置顶

## 博文封面
在`博文 Front-matter`中添加`cover: 图片地址`，若不配置则显示默认封面

在`主题配置文件`中修改封面设置
```yaml
cover:
  index_enable: true  #主页是否显示封面
  aside_enable: true  #不知道这是啥是否显示封面
  archives_enable: true  #归档页是否显示封面
  position: both  #主页封面显示位置left，right，both
  default_cover:  #默认封面地址
```
有多个默认封面地址时会随机选择封面
```yaml
default_cover:
  - 封面地址1
  - 封面地址2
  - 封面地址3...
```

# 博文页面相关

## 博文隐藏
按照文档安装插件 [hexo-hide-posts](https://github.com/printempw/hexo-hide-posts/blob/master/README_ZH.md)
后在`博文 Front-matter`中添加`hidden: true`

## 博文目录（TOC）
在`主题配置文件`中修改总博文目录设置
```yaml
toc:
  enable: true  #false完全关闭目录且无按钮
  number: true  #是否显示数字
  auto_open: true  #true就是默认自动打开目录，false默认关闭但有按钮可打开
```
在`博文 Front-matter`中可单独设置目录(不单独设置那一项即为默认)
```markdown
toc_number: true  #是否显示数字
toc: false  #false即为完全关闭目录，无按钮
auto_open: true  #true就是默认自动打开目录，false默认关闭但有按钮可打开
```

## 底部版权说明设置
博文如果不需要版权显示，在`博文 Front-matter`单独设置`copyright: false`

或者在`博文 Front-matter`单独设置详细版权(不单独设置那一项即为默认)
```markdown
copyright_author: xxxx
copyright_author_href: https://xxxxxx.com  #作者个人链接
copyright_url: https://xxxxxx.com  #文章链接
copyright_info: 此文章版权归xxxxx所有，如有转载，请注明来自原作者
```

# 主页头像
在`主题配置文件`中的`avatar`
```yaml
avatar:
  img: 图片地址
  effect: true #为true头像可以转圈
```

# Footer
在`主题配置信息`中的`footer`
```yaml
footer:
  owner:
    enable: true
    since: 2020  #起始年份
  custom_text:   #自定义内容（显示在第三行）
  copyright: true #是否开启版权（默认是“框架 Hexo|主题 Butterfly”）
  ICP:  #域名备案
      enable: true
      url: http://www.beian.miit.gov.cn/state/outPortal/loginPortal.action
      text: 粵ICP備xxxx
      icon: /img/icp.png
```

# 主页侧边栏

## 侧边排版
在`主题配置文件`中的`aside`
```yaml
side:
  enable: true  #是否开启侧边栏
  mobile: true  #手机上是否开启
  position: left  #left或者right
  card_author:  
    enable: true  #作者名片是否开启
    description:  #描述
    button:  #按钮设置
      icon: fab fa-github  #按钮图标
      text: Follow Me  #按钮内容
      link: https://github.com/xxxxxx  #按钮链接
  card_announcement:  #公告栏
    enable: true  #是否开启
    content: This is my Blog  #内容
  card_recent_post:  #最新文章
    enable: true  #是否开启
    limit: 5  #最新文章数量，若是0则显示全部文章
    sort: date  #根据发布日date分类或者更新时间updated分类
  card_categories:  #分类栏
    enable: true  #是否开启
    limit: 8  #分类数量，若是0则显示全部分类
    expand: none  # none/true/false
  card_tags:  #标签栏
    enable: true  #是否开启
    limit: 40  #标签数量，若是0则显示全部标签
    color: false  #开启后标签五颜六色
  card_archives:  #归档栏
    enable: true  #是否开启
    type: monthly  #按年份yearly归档或者按月份monthly归档
    format: MMMM YYYY  #显示YYYY年 MM月或者MM月 YYYY年
    order: -1  # Sort of order. 1, asc for ascending; -1, desc for descending
    limit: 8  #归档数量，若是0则显示全部归档
  card_webinfo: true  #是否开启网站信息栏
```

## 网站信息
在`主题配置文件`中的`busuanzi`
```yaml
busuanzi:
  site_uv: true  #网站访问量
  site_pv: true  #网站总访问量
  page_pv: true  #文章阅读量
```
网页运行时间，在`主题配置文件`中的`runtimeshow`
```yaml
runtimeshow:
  enable: true
  publish_date: 6/7/2018 00:00:00  #网页开通时间
  #格式: 月/日/年 时间
  #或 年/月/日 时间
```

# 外挂标签




