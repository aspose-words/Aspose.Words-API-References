---
title: XmlMapping
second_title: Aspose.Words for Java API 参考
description:指定用于在父结构化文档标记和存储在文档的自定义 XML 数据部分中的 XML 元素之间建立映射的信息。
type: docs
weight: 629
url: /zh/java/com.aspose.words/xmlmapping/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
java.lang.Cloneable
```
public class XmlMapping implements Cloneable
```

指定用于在父结构化文档标记和存储在文档的自定义 XML 数据部分中的 XML 元素之间建立映射的信息。

要了解更多信息，请访问**Structured Document Tags or Content Control**文档文章。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [delete()](#delete--) | 删除父结构化文档到 XML 数据的映射。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getCustomXmlPart()](#getCustomXmlPart--) | 返回父结构化文档标记映射到的自定义 XML 数据部分。 |
| [getPrefixMappings()](#getPrefixMappings--) | 返回 XML 命名空间前缀映射以评估[getXPath()](../../com.aspose.words/xmlmapping\#getXPath--). |
| [getStoreItemId()](#getStoreItemId--) | 为自定义 XML 数据部分指定自定义 XML 数据标识符，用于评估[getXPath()](../../com.aspose.words/xmlmapping\#getXPath--)表达。 |
| [getXPath()](#getXPath--) | 返回 XPath 表达式，对其求值以查找映射到父结构化文档标记的自定义 XML 节点。 |
| [hashCode()](#hashCode--) |  |
| [isMapped()](#isMapped--) | 退货**true**如果父结构化文档标记成功映射到 XML 数据。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping)](#setMapping-com.aspose.words.CustomXmlPart-java.lang.String-java.lang.String-) | 设置父结构化文档标签和自定义 XML 数据部件的 XML 节点之间的映射。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### delete() {#delete--}
```
public void delete()
```


删除父结构化文档到 XML 数据的映射。

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
### getCustomXmlPart() {#getCustomXmlPart--}
```
public CustomXmlPart getCustomXmlPart()
```


返回父结构化文档标记映射到的自定义 XML 数据部分。

**退货:**
[CustomXmlPart](../../com.aspose.words/customxmlpart) - 父结构化文档标记映射到的自定义 XML 数据部分。
### getPrefixMappings() {#getPrefixMappings--}
```
public String getPrefixMappings()
```


返回 XML 命名空间前缀映射以评估[getXPath()](../../com.aspose.words/xmlmapping\#getXPath--).指定前缀映射集，当针对文档中的自定义 XML 数据部分评估 XPath 表达式时，应使用该前缀映射来解释 XPath 表达式。

**退货:**
 java.lang.String - XML 命名空间前缀映射来评估[getXPath()](../../com.aspose.words/xmlmapping\#getXPath--).
### getStoreItemId() {#getStoreItemId--}
```
public String getStoreItemId()
```


为自定义 XML 数据部分指定自定义 XML 数据标识符，用于评估[getXPath()](../../com.aspose.words/xmlmapping\#getXPath--)表达。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getXPath() {#getXPath--}
```
public String getXPath()
```


返回 XPath 表达式，对其求值以查找映射到父结构化文档标记的自定义 XML 节点。

**退货:**
java.lang.String - XPath 表达式，用于查找映射到父结构化文档标记的自定义 XML 节点。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isMapped() {#isMapped--}
```
public boolean isMapped()
```


退货**true**如果父结构化文档标记成功映射到 XML 数据。

**退货:**
布尔值 -**true**如果父结构化文档标记成功映射到 XML 数据。
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping) {#setMapping-com.aspose.words.CustomXmlPart-java.lang.String-java.lang.String-}
```
public boolean setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping)
```


设置父结构化文档标签和自定义 XML 数据部件的 XML 节点之间的映射。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| customXmlPart | [CustomXmlPart](../../com.aspose.words/customxmlpart) | 要映射到的自定义 XML 数据部分。 |
| xPath | java.lang.String | 用于查找 XML 节点的 XPath 表达式。 |
| prefixMapping | java.lang.String | 用于评估 XPath 的 XML 命名空间前缀映射。 |

**退货:**
boolean - 指示父结构化文档标记是否成功映射到 XML 节点的标志。
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
