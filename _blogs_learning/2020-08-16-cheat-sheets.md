---
layout: lecture
# title: Awesome Cheat Sheets
# date: 2020-07-17 10:59:49 -0000
categories: learning
image: assets/images/data-science-cheat-sheets-thumbnail.jpg
author: zwdai
tags: [featured, projects]
---

# test name

<!-- Lightweight client-side loader that feature-detects and load polyfills only when necessary -->
<!-- <script src="https://cdn.jsdelivr.net/npm/@webcomponents/webcomponentsjs@2/webcomponents-loader.min.js"></script> -->

<!-- Load the element definition -->
<script type="module" src="https://cdn.jsdelivr.net/gh/zerodevx/zero-md@2/dist/zero-md.min.js"></script>

<!-- Simply set the `src` attribute to your MD file and win -->
<zero-md
    src="https://raw.githubusercontent.com/dull-bird/awesome-cheat-sheets/master/README.md">
    <template>
        <!-- Load external stylesheets with a `<link rel="stylesheet">` tag -->
        <link rel="stylesheet" href="ullday-irdbay.github.io/static/main.css">
        <link rel="stylesheet" href="ullday-irdbay.github.io/static/syntax.css">
        <!-- <link rel="stylesheet" href="highlight-styles.css"> -->
  </template>
</zero-md>

---

[Repository on GitHub](https://github.com/dull-bird/awesome-cheat-sheets).

You can import `markdown` file to your `markdown` or `html` file by using [`<zero-md>`](https://zerodevx.github.io/zero-md/):

{% highlight html %}
<!-- Lightweight client-side loader that feature-detects and load polyfills only when necessary -->
<script src="https://cdn.jsdelivr.net/npm/@webcomponents/webcomponentsjs@2/webcomponents-loader.min.js"></script>

<!-- Load the element definition -->
<script type="module" src="https://cdn.jsdelivr.net/gh/zerodevx/zero-md@1/src/zero-md.min.js"></script>

<!-- Simply set the `src` attribute to your MD file and win -->
<zero-md
css-urls='["https://example.com/styles/custom-markdown.css", "https://example.com/styles/custom-highlight.css"]'
src="path/to/.md"></zero-md>
{% endhighlight %}
