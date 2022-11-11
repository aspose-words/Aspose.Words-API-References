---
title: I字段UpdateCultureProvider
second_title: Aspose.Words for Java API 参考
description: 实现时提供了一个在特定字段更新期间应使用的对象。
type: docs
weight: 643
url: /zh/java/com.aspose.words/ifieldupdatecultureprovider/
---
```
public interface I字段UpdateCultureProvider
```

实施时，提供了一个[CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo)在更新特定字段期间应使用的对象。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [getCulture(String culture, 字段 field)](#getCulture-java.lang.String-com.aspose.words.字段-) | 返回一个[CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo)在字段更新期间使用的对象。 |
### getCulture(String culture, 字段 field) {#getCulture-java.lang.String-com.aspose.words.字段-}
```
public abstract System.Globalization.CultureInfo getCulture(String culture, 字段 field)
```


返回一个[CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo)在字段更新期间使用的对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| culture | java.lang.String | 为正在更新的字段请求的区域性名称。 |
| field | [字段](../../com.aspose.words/field) | 正在更新的字段。 |

**退货:**
[CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo) - 应该用于字段更新的文化对象。