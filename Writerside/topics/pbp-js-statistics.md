# 添加统计代码块

网站统计代码可以帮助网站管理员更好地了解用户需求和行为，优化网站内容和结构，提高用户体验和转化率，
同时也可以监控竞争对手的网站数据，调整自己的网站策略和优化方向。


## 统计代码作用

1. 了解网站流量情况：通过安装统计代码，可以实时了解网站的访问量、访客来源、访问时长等数据，帮助网站管理员了解网站的受欢迎程度和用户行为，从而进行网站优化和改进。
2. 优化网站内容：通过分析用户行为数据，可以了解用户对网站内容的兴趣和需求，从而优化网站的内容和结构，提高用户体验和转化率。
3. 监控竞争对手：通过分析竞争对手的网站数据，可以了解竞争对手的网站规模、访问量、用户行为等数据，从而调整自己的网站策略和优化方向。
4. 优化搜索引擎排名：通过安装统计代码并确保其在站内的每个页面上均添加了统计代码，可以让搜索引擎更加了解网站的页面结构和内容，从而提升搜索引擎的排名。



## 添加统计代码块


1. 在Writerside实例根目录创建文件：`cfg/buildprofiles.xml`  

```xml
<buildprofiles xsi:noNamespaceSchemaLocation="https://resources.jetbrains.com/writerside/1.0/build-profiles.xsd"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
    <variables>
        <analytics-head-script-file>head-script.html</analytics-head-script-file>
    </variables>
</buildprofiles>
```

2. 在cfg文件夹下创建文件`head-script.html`，文件名没有要求，与第一步的配置同名即可。   

```
<script>
    var _hmt = _hmt || [];
    (function() {
      var hm = document.createElement("script");
      hm.src = "https://hm.baidu.com/hm.js?9d3da7dfcdce3446d86f824xxxxxxxxx";
      var s = document.getElementsByTagName("script")[0];
      s.parentNode.insertBefore(hm, s);
    })();
</script>
```

这里以百度统计代码块为例。html文件中的内容会插入到每个文档的head标签中，

<tip>
既然可以在文档插入代码块，那么很多自定义功能都可以用这个方式实现了。
</tip>
