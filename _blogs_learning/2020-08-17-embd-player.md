---
layout: lecture
# title: "在GitHub Pages中嵌入bliiblii和youtube视频"
categories: [learning]
image: assets/images/bilibili_10_years.jpg
tags: [featured]
---

# 在GitHub Pages中嵌入bliiblii和youtube视频

## 1. bilibili

### 1.1. 获取代码

打开B站视频，并点击下方“分享”按钮。

<img src= "https://ullday-irdbay.github.io/assets/images/bilibili_分享.png" width="50%" alt="">

可以看到一个“嵌入代码”，复制它。

```html
<iframe src="//player.bilibili.com/player.html?aid=201491705&bvid=BV1Vh411Z7j5&cid=214635734&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>
```

可是如果直接把这段代码放到GitHub Page的post(`.md` 文件)中，得到的嵌入视频非常小，效果如下：

<iframe src="//player.bilibili.com/player.html?aid=201491705&bvid=BV1Vh411Z7j5&cid=214635734&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

### 1.2. 改进

添加额外的代码改进播放效果：

```html
<iframe src="//player.bilibili.com/player.html?aid=201491705&bvid=BV1Vh411Z7j5&cid=214635734&page=1&as_wide=1&high_quality=3&danmaku=0"
        allowfullscreen="allowfullscreen"
        width="100%" height="500"
        scrolling="no"
        frameborder="0"
        sandbox="allow-top-navigation allow-same-origin allow-forms allow-scripts">
</iframe>
```

效果：

<iframe src="//player.bilibili.com/player.html?aid=201491705&bvid=BV1Vh411Z7j5&cid=214635734&page=1&as_wide=1&high_quality=1&danmaku=0"
	allowfullscreen="allowfullscreen" width="100%" height="500" scrolling="no" frameborder="0" sandbox="allow-top-navigation allow-same-origin allow-forms allow-scripts"></iframe>
经过对比这两种方法的效果是一样的😅。

## 2. Youtube

Youtube视频的分享更加简单。同样点击视频下方的“分享”，然后选择“嵌入”。

<img src="https://dull-bird.github.io/assets/images/youtube-embd.png" width = "50%" alt="youtube">

直接将代码复制，粘贴到文章内即可。

```html
<iframe width="560" height="315" src="https://www.youtube.com/embed/dEhsFFEdd6Q" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

效果如下：

<iframe width="560" height="315" src="https://www.youtube.com/embed/dEhsFFEdd6Q" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
