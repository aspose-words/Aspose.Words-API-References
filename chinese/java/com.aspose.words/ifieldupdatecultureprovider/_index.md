---
title: IFieldUpdateCultureProvider
second_title: Aspose.Words for Java API 参考
description: 实现时提供了一个在特定字段更新期间应使用的对象。
type: docs
weight: 643
url: /zh/java/com.aspose.words/ifieldupdatecultureprovider/
---
```
public interface IFieldUpdateCultureProvider
```

实施时，提供[CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo)在更新特定字段期间应使用的对象。
## 方法

| 方法 | 描述 |
| --- | --- |
| [getCulture(String culture, Field field)](#getCulture-java.lang.String-com.aspose.words.Field-) | 返回一个[CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo)在字段更新期间使用的对象。 |
### getCulture(String culture, Field field) {#getCulture-java.lang.String-com.aspose.words.Field-}
```
public abstract System.Globalization.CultureInfo getCulture(String culture, Field field)
```


返回一个[CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo)在字段更新期间使用的对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| culture | java.lang.String | 为正在更新的字段请求的区域性名称。 |
| field | [Field](../../com.aspose.words/field) | 正在更新的字段。 |

**退货:**
[CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo) - 应该用于字段更新的文化对象。