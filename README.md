# 宅宅导航最新地址发布页分享及代码功能解析

## 这是一个简洁的导航发布页，设计用于展示宅宅导航的最新地址、备用地址和永久地址，用户可以通过页面快速访问相关链接。页面的整体设计简约清晰，适合桌面和移动设备使用。下面是详细的介绍：
**这个界面本来是有好多文件夹的，但是为了方便小白使用，我把文件夹都去掉了，然后把css文件也都集中在html里面，使其一个文件就能满足发布页的效果！下面是介绍、小样示例及代码：** <br>
小样示例页：https://bumilu66.buzz/宅宅导航最新地址发布页分享及代码功能解析/

## 页面结构介绍：
**头部信息（Meta 标签）：**

1.设置了页面字符集为 utf-8，确保页面能正确显示中文。<br>
2.设置了适合不同屏幕大小的 viewport，确保页面在移动端也能自适应显示。<br>
3.包含 description 和 keywords，用于 SEO 优化，提升页面在搜索引擎中的可见性。<br><br>
**背景图片：**

1.背景图片通过 background 属性设置为固定背景 (fixed)，图片位置居中 (center center) 且不随滚动条移动。<br>
2.背景图片占据整个页面视图 (background-size: cover)，使内容浮动在背景之上。<br><br>
**头像部分：**

1.一个圆形头像图片通过 .qqimg 类样式展示，头像位于页面顶部居中。<br>
2.使用圆形边框、阴影和白色背景突出头像，视觉上清爽简洁。<br><br>
**标题和副标题：**

1.大标题展示为“宅宅的导航引导页”，字体较大 (2.5em)，颜色为清新的蓝绿色。<br>
2.副标题展示为“一个人可以被打，但不能被打倒！” ，旨在增强页面的个性化氛围。<br><br>
**导航部分：**

1.导航部分通过无序列表```<ul>```列出各个链接地址，如“宅宅导航”、“最新地址”、“备用地址”和“永久地址”，用户可以点击这些链接快速跳转到指定页面。<br>
2.每个链接使用蓝色文字和浅色背景，带有悬停效果，悬停时链接背景变为深蓝色，文字颜色变为白色，增强了用户的交互体验。<br><br>

**联系信息：**

提供了联系邮箱，方便用户在有问题或需要帮助时联系。<br><br>
**版权信息：**

在页面底部提供了简单的版权声明，标明了版权所属以及年份。<br>
## 样式（CSS）说明：
**布局：** 使用了max-width 限制内容宽度为1200px，确保页面在大屏设备上不会显得过于空旷，同时使用了 margin: 0 auto; 保证内容在屏幕中间居中。<br><br>

**响应式设计：** 使用了媒体查询（@media (max-width: 768px)）对移动设备进行优化。移动设备上会调整导航菜单的布局为垂直排列，头像、标题和文字的大小也相应缩小，确保移动端用户的阅读体验。<br><br>

## 其他样式：

1.圆形头像边框 (border-radius: 50%) 和阴影效果 (box-shadow) 提升视觉层次感。<br>
2.悬停效果 (hover) 让导航链接具备更好的交互体验。<br><br>
**适用场景：**
该页面适合用于导航发布、链接引导页等类型的网页，特别是用于展示和引导用户访问不同的备用地址，确保用户在访问主站点遇到问题时能迅速找到备用站点。<br>

## 移动端优化：
页面使用了响应式设计，确保在手机或其他小屏幕设备上也能自适应显示，不需要用户左右滑动。<br>


```
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <meta name="description" content="宅宅导航发布页，宅宅导航超级入口,宅宅导航超级入口汇集了各种热门的网络娱乐资源，包括电影、电视剧、综艺节目、动漫、音乐等。 用户只需要在宅宅导航超级入口上输入自己感兴趣的内">
    <meta name="keywords" content="宅宅导航, 宅宅导航最新地址发布页,最新地址, 备用地址, 永久地址">
    <title>宅宅导航发布页</title>
    <link rel="stylesheet" type="text/css" href="static/css/style.css">
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background: url('bg3.png') no-repeat center center fixed;
            background-size: cover;
            text-align: center; /* 确保文本居中 */
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            background: rgba(255, 255, 255, 0); /* 添加背景遮罩，确保内容可见 */
            box-sizing: border-box; /* 确保内边距不会影响宽度 */
        }

        .qqimg {
            margin: 0 auto;
            width: 150px;
            height: 150px;
            border-radius: 50%;
            overflow: hidden;
            border: 5px solid #fff;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            background: #fff;
        }

        .qqimg img {
            width: 100%;
            height: auto;
            display: block;
        }

        .title h1 {
            font-size: 2.5em;
            color: #4ca6a7;
            margin-top: 20px;
        }

        .title p {
            font-size: 1.2em;
            color: #777;
        }

        .nav {
            margin-top: 30px;
        }

        .nav ul {
            list-style: none;
            padding: 0;
        }

        .nav ul li {
            display: inline-block;
            margin: 10px 20px;
        }

        .nav ul li a {
            text-decoration: none;
            font-size: 1.2em;
            color: #007bff;
            padding: 10px 20px;
            background-color: #f8f9fa;
            border-radius: 8px;
            transition: background-color 0.3s, color 0.3s;
        }

        .nav ul li a:hover {
            background-color: #0056b3;
            color: #fff;
        }

        .contact h3 {
            margin-top: 30px;
            font-size: 1.1em;
            color: #adbb41;
        }

        .solid-wh, .solid-ht {
            height: 20px;
        }

        .copyright {
            margin-top: 30px;
            color: #999;
            font-size: 0.9em;
        }

        /* 调整整体间距 */
        .spacer {
            margin-top: 40px;
        }

        /* 为移动端优化布局 */
        @media (max-width: 768px) {
            .nav ul li {
                display: block;
                margin: 10px 0;
            }

            .qqimg {
                width: 120px;
                height: 120px;
            }

            .title h1 {
                font-size: 2em;
            }

            .title p {
                font-size: 1em;
            }

            .nav ul li a {
                font-size: 1em;
                padding: 4px 15px;
            }
        }
    </style>
</head>

<body>

    <div class="container">
        <div class="qqimg">
            <img src="tx.webp" alt="宅宅头像">
        </div>
        
        <div class="spacer"></div>
        
        <div class="title">
            <h1>宅宅的导航引导页</h1>
            <p>但行前路，不负韶华！</p>
        </div>

        <div class="spacer"></div>
        
        <div class="nav">
            <ul>
                <li>
                    <a href="https://google.com" target="_blank">宅宅导航</a>
                </li>
                <li>
                    <a href="https://google.com" target="_blank">最新地址</a>
                </li>
                <li>
                    <a href="https://google.com" target="_blank">备用地址</a>
                </li>
                <li>
                    <a href="https://google.com" target="_blank">永久地址</a>
                </li>
            </ul>
        </div>

        <div class="contact">
            <h3>联系邮箱：123456@gmail.com</h3>
        </div>

        <div class="copyright">
            <p>Copyright © 2023-2024. https://google.com</p>
        </div>
    </div>

</body>
</html>
```
