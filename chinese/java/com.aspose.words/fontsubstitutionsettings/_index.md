---
title: FontSubstitutionSettings
second_title: Aspose.Words for Java API Reference
description: 指定字体替换机制设置。
type: docs
weight: 290
url: /zh/java/com.aspose.words/fontsubstitutionsettings/
---

**遗产:**
java.lang.Object
```
public class FontSubstitutionSettings
```

指定字体替换机制设置。

要了解更多信息，请访问**Working with Fonts**文档文章。

字体替换过程由几个规则组成，这些规则按特定顺序一一检查。如果第一条规则无法解析字体，则检查第二条规则，依此类推。

规则顺序如下： 1. 字体名称替换规则（默认开启） 2. 字体配置替换规则（默认关闭） 3. 表格替换规则（默认开启） 4. 字体信息替换规则（默认开启） ) 5. 默认字体规则（默认开启）

请注意，字体信息替换规则将始终解析字体，如果[FontInfo](../../com.aspose.words/fontinfo)可用并将覆盖默认字体规则。如果要使用默认字体规则，则应禁用字体信息替换规则。

请注意，字体配置替换规则将在大多数情况下解析字体，从而覆盖所有其他规则。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getDefaultFontSubstitution()](#getDefaultFontSubstitution--) | 与默认字体替换规则相关的设置。 |
| [getFontConfigSubstitution()](#getFontConfigSubstitution--) | 与字体配置替换规则相关的设置。 |
| [getFontInfoSubstitution()](#getFontInfoSubstitution--) | 与字体信息替换规则相关的设置。 |
| [getFontNameSubstitution()](#getFontNameSubstitution--) | 与字体名称替换规则相关的设置。 |
| [getTableSubstitution()](#getTableSubstitution--) | 与表替换规则相关的设置。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getDefaultFontSubstitution() {#getDefaultFontSubstitution--}
```
public DefaultFontSubstitutionRule getDefaultFontSubstitution()
```


与默认字体替换规则相关的设置。

**退货:**
[DefaultFontSubstitutionRule](../../com.aspose.words/defaultfontsubstitutionrule) - 相应的[DefaultFontSubstitutionRule](../../com.aspose.words/defaultfontsubstitutionrule)价值。
### getFontConfigSubstitution() {#getFontConfigSubstitution--}
```
public FontConfigSubstitutionRule getFontConfigSubstitution()
```


与字体配置替换规则相关的设置。

**退货:**
[FontConfigSubstitutionRule](../../com.aspose.words/fontconfigsubstitutionrule) - 相应的[FontConfigSubstitutionRule](../../com.aspose.words/fontconfigsubstitutionrule)价值。
### getFontInfoSubstitution() {#getFontInfoSubstitution--}
```
public FontInfoSubstitutionRule getFontInfoSubstitution()
```


与字体信息替换规则相关的设置。

**退货:**
[FontInfoSubstitutionRule](../../com.aspose.words/fontinfosubstitutionrule) - 相应的[FontInfoSubstitutionRule](../../com.aspose.words/fontinfosubstitutionrule)价值。
### getFontNameSubstitution() {#getFontNameSubstitution--}
```
public FontNameSubstitutionRule getFontNameSubstitution()
```


与字体名称替换规则相关的设置。

**退货:**
[FontNameSubstitutionRule](../../com.aspose.words/fontnamesubstitutionrule) - 相应的[FontNameSubstitutionRule](../../com.aspose.words/fontnamesubstitutionrule)价值。
### getTableSubstitution() {#getTableSubstitution--}
```
public TableSubstitutionRule getTableSubstitution()
```


与表替换规则相关的设置。

**退货:**
[TableSubstitutionRule](../../com.aspose.words/tablesubstitutionrule) - 相应的[TableSubstitutionRule](../../com.aspose.words/tablesubstitutionrule)价值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
