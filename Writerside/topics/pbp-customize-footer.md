# 自定义页脚



一般网站底部一般包括以下内容：

1. 版权信息：例如“© 版权所有”等。
2. 联系信息：包括电话号码、电子邮件地址、联系地址或社交媒体链接等。
3. 导航菜单：可以方便访问者浏览网站，包括网站的主要分类或页面链接等。
4. 友情链接：在底部使用较多的文本链接，有利于优化。
5. 品牌宣传：可以放置企业的logo或者是一些图形去做品牌宣传。
6. 联系方式：可以放置电话号码、邮箱、地址等一些基本的信息。

使用Writerside自定义页脚，也是可以自定义添加内容的。

## 添加备案号

下面示例展示了邮箱与网站备案号。

示例效果

![pbp-customize-footer-001.png](pbp-customize-footer-001.png)

配置代码

```xml 

<buildprofiles xsi:noNamespaceSchemaLocation="https://resources.jetbrains.com/writerside/1.0/build-profiles.xsd"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
    <build-profile instance="w"></build-profile>
    <footer>
        <copyright>2023-2024 writerside.cn</copyright>
        <icp>沪ICP备19002970号-6</icp>
        <social type="email" href="zengs@mosong.cc">联系邮箱</social>
    </footer>
</buildprofiles>
```

<!-- 
https://www.jetbrains.com/help/writerside/customize-the-footer.html
-->