# 自定义Logo

设置自己的网站logo与网站favicon。


## 设置Logo

可以在文档名称旁边的标题中显示公司、产品或项目的Logo。

1. 把logo图片放到项目的`images`目录中。

<note>
Logo图片要求如下:
<ul>
    <li>SVG或PNG格式。建议使用SVG以获得更好的效果。</li>
    <li>高宽比在1.2和0.24之间。建议使用方形图。</li>
    <li>图片高度大于48px。</li>
</ul>

</note>

2. 打开文件`cfg/buildprofiles.xml`。
3. 使用`<variables>`下的`<header-logo>`元素指定图片文件名。

```xml

<header-logo>my-logo.png</header-logo>
```

4. 如果你希望给logo图片加上链接，可以使用`<product-web-url>`

```xml

<product-web-url>https://writerside.cn</product-web-url>
```

点击文档的LOGO图片，则会跳转这个链接，一般情况会配置文档的首页地址。

## 设置favicon

<note>
支持的格式有SVG、PNG和ICO。  

可以使用多个不同尺寸的图标:16x16, 32x32, 96x96, 300x300
</note>

单个本地icon文件:

```xml

<custom-favicons>favicon.png</custom-favicons>
```

单个icon文件URL:

```xml

<custom-favicons>https://writerside.cn/icon.svg</custom-favicons>
```

多个icon文件按大小排序:

```xml

<custom-favicons>icon16.png,icon32.png,icon96.png,icon300.png</custom-favicons>
```

## 配置文件

配置完成后，`cfg/buildprofiles.xml`完整文件内容如下

```xml

<buildprofiles xsi:noNamespaceSchemaLocation="https://resources.jetbrains.com/writerside/1.0/build-profiles.xsd"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
    <build-profile instance="w"></build-profile>
    <variables>
        <custom-favicons>favicon.png</custom-favicons>
        <header-logo>writerside.svg</header-logo>
        <product-web-url>https://writerside.cn</product-web-url>
    </variables>
</buildprofiles>
```

<tip>
提示：可以去查看 buildprofiles.xml 文件对应的xsd文件，了解更多可配置的属性。
</tip>


