---
title: CustomPart
second_title: Aspose.Words for Java API 参考
description: 表示 ISO/IEC 29500 标准未定义的自定义任意内容部分。
type: docs
weight: 102
url: /zh/java/com.aspose.words/custompart/
---

**遗产:**
java.lang.Object

**所有实现的接口:**
java.lang.Cloneable
```
public class CustomPart implements Cloneable
```

表示 ISO/IEC 29500 标准未定义的自定义（任意内容）部分。

要了解更多信息，请访问**Structured Document Tags or Content Control**文档文章。

此类表示作为“未知关系”目标的 OOXML 部分。 ISO/IEC 29500 中未定义的所有关系都被视为“未知关系”。未知关系在 Office Open XML 文档中是允许的，前提是它们符合关系标记准则。

Microsoft Word 在打开/保存周期中保留自定义部分。可以在此处找到一些其他信息 http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

 Aspose.Words 还往返自定义部件，此外，允许通过编程方式访问这些部件[CustomPart](../../com.aspose.words/custompart)和[CustomPartCollection](../../com.aspose.words/custompartcollection)对象。

不要将自定义部件与自定义 XML 数据混淆。利用[CustomXmlPart](../../com.aspose.words/customxmlpart)如果您需要访问自定义 XML 数据。
## 方法

| 方法 | 描述 |
| --- | --- |
| [deepClone()](#deepClone--) | 制作对象的“足够深”的副本。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getContentType()](#getContentType--) | 指定此自定义部件的内容类型。 |
| [getData()](#getData--) | 包含此自定义部件的数据。 |
| [getName()](#getName--) | 获取此部分在 OOXML 包或目标 URL 中的绝对名称。 |
| [getRelationshipType()](#getRelationshipType--) | 获取从父部件到此自定义部件的关系类型。 |
| [hashCode()](#hashCode--) |  |
| [isExternal()](#isExternal--) | \{ 如果此自定义部分存储在 OOXML 包中，则为 False。 |
| [isExternal(boolean value)](#isExternal-boolean-) | \{ 如果此自定义部分存储在 OOXML 包中，则为 False。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setContentType(String value)](#setContentType-java.lang.String-) | 指定此自定义部件的内容类型。 |
| [setData(byte[] value)](#setData-byte---) | 包含此自定义部件的数据。 |
| [setName(String value)](#setName-java.lang.String-) | 在 OOXML 包或目标 URL 中设置此部分的绝对名称。 |
| [setRelationshipType(String value)](#setRelationshipType-java.lang.String-) | 设置从父部件到此自定义部件的关系类型。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### deepClone() {#deepClone--}
```
public CustomPart deepClone()
```


制作对象的“足够深”的副本。不重复的字节[getData()](../../com.aspose.words/custompart\#getData--) / [setData(byte[])](../../com.aspose.words/custompart\#setData-byte---)价值。

**退货:**
[CustomPart](../../com.aspose.words/custompart)
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getContentType() {#getContentType--}
```
public String getContentType()
```


指定此自定义部件的内容类型。

此属性仅适用于[isExternal()](../../com.aspose.words/custompart\#isExternal--) / [isExternal(boolean)](../../com.aspose.words/custompart\#isExternal-boolean-)是假的。

默认值为空字符串。有效值必须是非空字符串。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getData() {#getData--}
```
public byte[] getData()
```


包含此自定义部件的数据。

此属性仅适用于[isExternal()](../../com.aspose.words/custompart\#isExternal--) / [isExternal(boolean)](../../com.aspose.words/custompart\#isExternal-boolean-)是假的。

默认值为空字节数组。该值不能为 null 。

**退货:**
字节[- 对应的字节[] 价值。
### getName() {#getName--}
```
public String getName()
```


获取此部分在 OOXML 包或目标 URL 中的绝对名称。

如果关系目标是内部的，则此属性是包内的绝对部件名称。如果关系目标是外部的，则此属性是目标 URL。

默认值为空字符串。有效值必须是非空字符串。

**退货:**
java.lang.String - 此部分在 OOXML 包或目标 URL 中的绝对名称。
### getRelationshipType() {#getRelationshipType--}
```
public String getRelationshipType()
```


获取从父部件到此自定义部件的关系类型。

自定义部件的关系类型必须是“未知的”，例如自定义关系类型，而不是 ISO/IEC 29500 中定义的关系类型之一。

默认值为空字符串。有效值必须是非空字符串。

**退货:**
java.lang.String - 从父部件到此自定义部件的关系类型。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isExternal() {#isExternal--}
```
public boolean isExternal()
```


\{ 如果此自定义部件存储在 OOXML 包中，则为 False。如果此自定义部件是外部目标，则为真。

默认值为 false 。

**退货:**
boolean - 对应的布尔值。
### isExternal(boolean value) {#isExternal-boolean-}
```
public void isExternal(boolean value)
```


\{ 如果此自定义部件存储在 OOXML 包中，则为 False。如果此自定义部件是外部目标，则为真。

默认值为 false 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setContentType(String value) {#setContentType-java.lang.String-}
```
public void setContentType(String value)
```


指定此自定义部件的内容类型。

此属性仅适用于[isExternal()](../../com.aspose.words/custompart\#isExternal--) / [isExternal(boolean)](../../com.aspose.words/custompart\#isExternal-boolean-)是假的。

默认值为空字符串。有效值必须是非空字符串。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setData(byte[] value) {#setData-byte---}
```
public void setData(byte[] value)
```


包含此自定义部件的数据。

此属性仅适用于[isExternal()](../../com.aspose.words/custompart\#isExternal--) / [isExternal(boolean)](../../com.aspose.words/custompart\#isExternal-boolean-)是假的。

默认值为空字节数组。该值不能为 null 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | byte[] | 对应字节[] 价值。 |

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


在 OOXML 包或目标 URL 中设置此部分的绝对名称。

如果关系目标是内部的，则此属性是包内的绝对部件名称。如果关系目标是外部的，则此属性是目标 URL。

默认值为空字符串。有效值必须是非空字符串。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 此部分在 OOXML 包或目标 URL 中的绝对名称。 |

### setRelationshipType(String value) {#setRelationshipType-java.lang.String-}
```
public void setRelationshipType(String value)
```


设置从父部件到此自定义部件的关系类型。

自定义部件的关系类型必须是“未知的”，例如自定义关系类型，而不是 ISO/IEC 29500 中定义的关系类型之一。

默认值为空字符串。有效值必须是非空字符串。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 从父部件到此自定义部件的关系类型。 |

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
