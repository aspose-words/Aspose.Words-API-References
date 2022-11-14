---
title: Style
second_title: Aspose.Words for Java API 参考
description: 表示单个内置或用户定义的样式。
type: docs
weight: 536
url: /zh/java/com.aspose.words/style/
---

**遗产:**
java.lang.Object

**所有实现的接口:**
java.lang.Cloneable
```
public class Style implements Cloneable
```

表示单个内置或用户定义的样式。

要了解更多信息，请访问**Working with Styles and Themes**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [clearParaAttrs()](#clearParaAttrs--) |  |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [equals(Style style)](#equals-com.aspose.words.Style-) | 与指定样式进行比较。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int-) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int-) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int-) |  |
| [getAliases()](#getAliases--) | 获取此样式的所有别名。 |
| [getBaseStyleName()](#getBaseStyleName--) | 获取/设置此样式所基于的样式的名称。 |
| [getBuiltIn()](#getBuiltIn--) | 如果此样式是 MS Word 中的内置样式之一，则为真。 |
| [getClass()](#getClass--) |  |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int-) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int-) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int-) |  |
| [getDocument()](#getDocument--) | 获取所有者文档。 |
| [getFont()](#getFont--) | 获取样式的字符格式。 |
| [getLinkedStyleName()](#getLinkedStyleName--) | 获取链接到此样式的样式的名称。 |
| [getList()](#getList--) | 获取定义此列表样式格式的列表。 |
| [getListFormat()](#getListFormat--) | 提供对段落样式的列表格式属性的访问。 |
| [getName()](#getName--) | 获取样式的名称。 |
| [getNextParagraphStyleName()](#getNextParagraphStyleName--) | 获取/设置要自动应用于在使用指定样式格式化的段落之后插入的新段落的样式的名称。 |
| [getParagraphFormat()](#getParagraphFormat--) | 获取样式的段落格式。 |
| [getStyleIdentifier()](#getStyleIdentifier--) | 获取内置样式的区域独立样式标识符。 |
| [getStyles()](#getStyles--) | 获取此样式所属的样式集合。 |
| [getType()](#getType--) | 获取样式类型（段落或字符）。 |
| [hashCode()](#hashCode--) |  |
| [isHeading()](#isHeading--) | 当样式是内置标题样式之一时为真。 |
| [isQuickStyle()](#isQuickStyle--) | 指定此样式是否显示在 MS Word UI 内的快速样式库中。 |
| [isQuickStyle(boolean value)](#isQuickStyle-boolean-) | 指定此样式是否显示在 MS Word UI 内的快速样式库中。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | 从文档中删除指定的样式。 |
| [removeParaAttr(int key)](#removeParaAttr-int-) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [setBaseStyleName(String value)](#setBaseStyleName-java.lang.String-) | 获取/设置此样式所基于的样式的名称。 |
| [setName(String value)](#setName-java.lang.String-) | 设置样式的名称。 |
| [setNextParagraphStyleName(String value)](#setNextParagraphStyleName-java.lang.String-) | 获取/设置要自动应用于在使用指定样式格式化的段落之后插入的新段落的样式的名称。 |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object-) |  |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearParaAttrs() {#clearParaAttrs--}
```
public void clearParaAttrs()
```




### clearRunAttrs() {#clearRunAttrs--}
```
public void clearRunAttrs()
```




### equals(Style style) {#equals-com.aspose.words.Style-}
```
public boolean equals(Style style)
```


与指定的样式进行比较。样式 Istd 仅针对内置样式进行比较。样式默认值不包括在比较中。递归比较基本样式、链接样式和下一段样式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| style | [Style](../../com.aspose.words/style) |  |

**退货:**
布尔值
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
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int-}
```
public Object fetchInheritedParaAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### fetchParaAttr(int key) {#fetchParaAttr-int-}
```
public Object fetchParaAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getAliases() {#getAliases--}
```
public String[] getAliases()
```


获取此样式的所有别名。如果 style 没有别名，则返回空字符串数组。

**退货:**
java.lang.String[] - 此样式的所有别名。
### getBaseStyleName() {#getBaseStyleName--}
```
public String getBaseStyleName()
```


获取/设置此样式所基于的样式的名称。如果样式不基于任何其他样式，这将是一个空字符串，并且可以将其设置为空字符串。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getBuiltIn() {#getBuiltIn--}
```
public boolean getBuiltIn()
```


如果此样式是 MS Word 中的内置样式之一，则为真。

**退货:**
boolean - 对应的布尔值。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getDirectParaAttr(int key) {#getDirectParaAttr-int-}
```
public Object getDirectParaAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int-}
```
public Object getDirectParaAttr(int key, int revisionsView)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**退货:**
java.lang.Object
### getDirectRunAttr(int key) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


获取所有者文档。

**退货:**
[DocumentBase](../../com.aspose.words/documentbase) - 所有者文档。
### getFont() {#getFont--}
```
public Font getFont()
```


获取样式的字符格式。

对于列表样式，此属性返回 null。

**退货:**
[Font](../../com.aspose.words/font) - 样式的字符格式。
### getLinkedStyleName() {#getLinkedStyleName--}
```
public String getLinkedStyleName()
```


获取链接到这个样式的名称。如果没有链接样式，则返回空字符串。

**退货:**
java.lang.String - 链接到此样式的样式的名称。
### getList() {#getList--}
```
public List getList()
```


获取定义此列表样式格式的列表。

此属性仅对列表样式有效。对于其他样式类型，此属性返回 null。

**退货:**
[List](../../com.aspose.words/list) - 定义此列表样式格式的列表。
### getListFormat() {#getListFormat--}
```
public ListFormat getListFormat()
```


提供对段落样式的列表格式属性的访问。

此属性仅对段落样式有效。对于其他样式类型，此属性返回 null。

**退货:**
[ListFormat](../../com.aspose.words/listformat) - 相应的[ListFormat](../../com.aspose.words/listformat)价值。
### getName() {#getName--}
```
public String getName()
```


获取样式的名称。

不能为空字符串。

如果集合中已经存在同名的样式，则该样式将覆盖它。所有受影响的节点都将引用新样式。

**退货:**
java.lang.String - 样式的名称。
### getNextParagraphStyleName() {#getNextParagraphStyleName--}
```
public String getNextParagraphStyleName()
```


获取/设置要自动应用于在使用指定样式格式化的段落之后插入的新段落的样式的名称。 Aspose.Words 不使用该属性。仅当您在 MS Word 中编辑文档时，才会自动应用下一段样式。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getParagraphFormat() {#getParagraphFormat--}
```
public ParagraphFormat getParagraphFormat()
```


获取样式的段落格式。

对于字符和列表样式，此属性返回 null。

**退货:**
[ParagraphFormat](../../com.aspose.words/paragraphformat) - 样式的段落格式。
### getStyleIdentifier() {#getStyleIdentifier--}
```
public int getStyleIdentifier()
```


获取内置样式的区域独立样式标识符。

对于用户定义（自定义）样式，此属性返回[StyleIdentifier.USER](../../com.aspose.words/styleidentifier\#USER).

**退货:**
int - 内置样式的独立于语言环境的样式标识符。返回值是以下之一[StyleIdentifier](../../com.aspose.words/styleidentifier)常数。
### getStyles() {#getStyles--}
```
public StyleCollection getStyles()
```


获取此样式所属的样式集合。

**退货:**
[StyleCollection](../../com.aspose.words/stylecollection) 此样式所属的样式集合。
### getType() {#getType--}
```
public int getType()
```


获取样式类型（段落或字符）。

**退货:**
 int - 样式类型（段落或字符）。返回值是以下之一[StyleType](../../com.aspose.words/styletype)常数。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isHeading() {#isHeading--}
```
public boolean isHeading()
```


当样式是内置标题样式之一时为真。

**退货:**
boolean - 对应的布尔值。
### isQuickStyle() {#isQuickStyle--}
```
public boolean isQuickStyle()
```


指定此样式是否显示在 MS Word UI 内的快速样式库中。

**退货:**
boolean - 对应的布尔值。
### isQuickStyle(boolean value) {#isQuickStyle-boolean-}
```
public void isQuickStyle(boolean value)
```


指定此样式是否显示在 MS Word UI 内的快速样式库中。

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




### remove() {#remove--}
```
public void remove()
```


从文档中删除指定的样式。样式移除对文档模型有以下影响：

 *  从相应的段落、运行和表格中删除对样式的所有引用。
 *  如果删除基本样式，则其格式将移至子样式。
 *  如果要删除的样式具有链接样式，则这两个样式都将被删除。

### removeParaAttr(int key) {#removeParaAttr-int-}
```
public void removeParaAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

### setBaseStyleName(String value) {#setBaseStyleName-java.lang.String-}
```
public void setBaseStyleName(String value)
```


获取/设置此样式所基于的样式的名称。如果样式不基于任何其他样式，这将是一个空字符串，并且可以将其设置为空字符串。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


设置样式的名称。

不能为空字符串。

如果集合中已经存在同名的样式，则该样式将覆盖它。所有受影响的节点都将引用新样式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 样式的名称。 |

### setNextParagraphStyleName(String value) {#setNextParagraphStyleName-java.lang.String-}
```
public void setNextParagraphStyleName(String value)
```


获取/设置要自动应用于在使用指定样式格式化的段落之后插入的新段落的样式的名称。 Aspose.Words 不使用该属性。仅当您在 MS Word 中编辑文档时，才会自动应用下一段样式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object-}
```
public void setParaAttr(int key, Object value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int key, Object value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

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
