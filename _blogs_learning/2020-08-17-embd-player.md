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

<img src= "https://dull-bird.github.io/assets/images/bilibili_分享.png" width="50%" alt="">

可以看到一个“嵌入代码”，复制它。

```html
<iframe src="//player.bilibili.com/player.html?aid=201491705&bvid=BV1Vh411Z7j5&cid=214635734&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>
```

可是如果直接把这段代码放到GitHub Page的post(`.md` 文件)中，得到的嵌入视频非常小，效果如下：

<iframe src="//player.bilibili.com/player.html?aid=201491705&bvid=BV1Vh411Z7j5&cid=214635734&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

### 1.2. 改进

我们可以在主题的`main.css`文件中添加以下代码（[来源](https://agong.me/2019/embeds-bilibili-video-to-wordpress.html)）：

```css
/* added for iframes */
.video-ratio {
position: relative;
width: 100%;
height: 0;
padding-bottom: 76%;
}

.video-ratio iframe {
position: absolute;
width: 100%;
height: 100%;
left: 0;
top: 0;
}
```

我们分别测试这两种`class`的效果（注意这里我们给嵌入视频加入了`high_quality=1`的标签，使得视频默认高清播放）：

#### 1.2.1. `video-ratio`

代码：

```html
<div class="video-ratio">
    <iframe src="//player.bilibili.com/player.html?aid=201491705&bvid=BV1Vh411Z7j5&cid=214635734&page=1&high_quality=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>
</div>
```

效果：

<div class="video-ratio">
    <iframe width="560" height="315" src="//player.bilibili.com/player.html?aid=201491705&bvid=BV1Vh411Z7j5&cid=214635734&page=1&high_quality=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>
</div>

#### 1.2.2. `video-ratio iframe`

代码：

```html
<div class="video-ratio iframe">
    <iframe src="//player.bilibili.com/player.html?aid=201491705&bvid=BV1Vh411Z7j5&cid=214635734&page=1&high_quality=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>
</div>
```

效果：

<div class="video-ratio iframe">
    <iframe src="//player.bilibili.com/player.html?aid=201491705&bvid=BV1Vh411Z7j5&cid=214635734&page=1&high_quality=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>
</div>

<iframe width="560" height="315" src="//player.bilibili.com/player.html?aid=201491705&bvid=BV1Vh411Z7j5&cid=214635734&page=1&high_quality=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

<iframe allowfullscreen="allowfullscreen"
    sandbox="allow-top-navigation allow-same-origin allow-forms allow-scripts"
    src="//player.bilibili.com/player.html?aid=330753250&bvid=BV1rA411s78W&cid=271030134&page=1"> </iframe>
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
