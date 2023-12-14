# 声明变量

变量是具有唯一名称的命名值，可以在文档中的不同位置使用。
当你改变它的值时，它会在所有文档中改变。


建议放入变量中内容:
- 版本号
- 产品名称或者公司名称
- 联系邮箱或者电话
- 提供的服务


使用全局常量参数，实现全局内容替换，比如文档名称，需要在多个地方用到，使用变量替换，可以实现全局修改。


## 1.声明变量

- 在文档根目录文件`v.list`中定义全局变量
```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE vars SYSTEM "https://resources.jetbrains.com/writerside/1.0/vars.dtd">
<vars>
    <var name="product" value="Writerside"/>
    <var name="website" value="https://writerside.cn"/>
</vars>

```
这里定义了  
变量名`product`，变量值`Writerside`    
变量名`website`，变量值`https://writerside.cn`    

可以使用标签`var`定义更多全局变量。

- 定义本地变量

本地变量只能在当前文档使用，在使用之前声明即可。
```
定义变量
<var name="latest" value="1.2"/>

使用变量
%\latest%

```



## 2.使用变量

变量定义好后，可以在所有文档中使用。

使用方法如下：
```
此文档名称是：%\product%，访问域名是：%\website%
```

展示结果示例：  
```
此文档名称是：%product%，访问域名是：%website%
```

## 3.忽略变量

比如写这个文档时，要写使用变量方法的示例，需要忽略变量避免被编码。 可以在变量第一个`%`后加上转义符`\\`即可。    

示例：`%\ product%`  （为了这个示例完整展示，给中间加了一个空格，实际不需要空格）




<!-- 参考： https://www.jetbrains.com/help/writerside/variables.html -->



