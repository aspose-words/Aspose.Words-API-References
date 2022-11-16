---
title: List
second_title: Aspose.Words for Java API 参考
description: 表示列表的格式。
type: docs
weight: 368
url: /zh/java/com.aspose.words/list/
---

**遗产：**
java.lang.Object

**所有已实现的接口：**
java.lang.Cloneable, java.lang.Comparable
```
public class List implements Cloneable, Comparable
```

表示列表的格式。

要了解更多信息，请访问**Working with Lists**文档文章。

Microsoft Word 文档中的列表是一组列表格式属性。每个列表最多可以有 9 个级别，并且为每个级别分别定义格式属性，例如数字样式、起始值、缩进、制表符位置等。

一个[List](../../com.aspose.words/list)对象总是属于[ListCollection](../../com.aspose.words/listcollection)收藏。

要创建新列表，请使用[ListCollection](../../com.aspose.words/listcollection)收藏。

要修改列表的格式，请使用[ListLevel](../../com.aspose.words/listlevel)在中找到的对象[getListLevels()](../../com.aspose.words/list\#getListLevels--)收藏。

要应用或删除段落中的列表格式，请使用[ListFormat](../../com.aspose.words/listformat).
## 方法

| 方法 | 描述 |
| --- | --- |
| [compareTo(List other)](#compareTo-com.aspose.words.List-) | 将指定列表与当前列表进行比较。 |
| [equals(List list)](#equals-com.aspose.words.List-) | 与指定列表进行比较。 |
| [equals(Object obj)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDocument()](#getDocument--) | 获取所有者文档。 |
| [getListId()](#getListId--) | 获取列表的唯一标识符。 |
| [getListLevels()](#getListLevels--) | 获取此列表的列表级别集合。 |
| [getStyle()](#getStyle--) | 获取此列表引用或定义的列表样式。 |
| [hasSameTemplate(List other)](#hasSameTemplate-com.aspose.words.List-) | 如果当前列表和给定列表是从同一模板创建的，则返回 true。 |
| [hashCode()](#hashCode--) |  |
| [isListStyleDefinition()](#isListStyleDefinition--) | 如果此列表是列表样式的定义，则返回 true。 |
| [isListStyleReference()](#isListStyleReference--) | 如果此列表是对列表样式的引用，则返回 true。 |
| [isMultiLevel()](#isMultiLevel--) | 当列表包含 9 个级别时返回 true； 1 级时为假。 |
| [isRestartAtEachSection()](#isRestartAtEachSection--) | 指定是否应在每个部分重新启动列表。 |
| [isRestartAtEachSection(boolean value)](#isRestartAtEachSection-boolean-) | 指定是否应在每个部分重新启动列表。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### compareTo(List other) {#compareTo-com.aspose.words.List-}
```
public int compareTo(List other)
```


将指定列表与当前列表进行比较。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| other | [List](../../com.aspose.words/list) |  |

**退货：**
整数
### equals(List list) {#equals-com.aspose.words.List-}
```
public boolean equals(List list)
```


与指定列表进行比较。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| list | [List](../../com.aspose.words/list) |  |

**退货：**
布尔值
### equals(Object obj) {#equals-java.lang.Object-}
```
public boolean equals(Object obj)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| obj | java.lang.Object |  |

**退货：**
布尔值
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


获取所有者文档。

列表始终具有父文档，并且仅在该文档的上下文中有效。

**退货：**
[DocumentBase](../../com.aspose.words/documentbase) - 所有者文件。
### getListId() {#getListId--}
```
public int getListId()
```


获取列表的唯一标识符。

您通常不需要使用此属性。但是如果你使用它，你通常会与[ListCollection.getListByListId(int)](../../com.aspose.words/listcollection\#getListByListId-int-)通过标识符查找列表的方法。

**退货：**
int - 列表的唯一标识符。
### getListLevels() {#getListLevels--}
```
public ListLevelCollection getListLevels()
```


获取此列表的列表级别集合。

使用此属性可以访问和修改每个列表级别的单独格式。

**退货：**
[ListLevelCollection](../../com.aspose.words/listlevelcollection) - 此列表的列表级别的集合。
### getStyle() {#getStyle--}
```
public Style getStyle()
```


获取此列表引用或定义的列表样式。

如果此列表未与列表样式关联，则该属性将返回 null。

列表可以是对列表样式的引用，在这种情况下[isListStyleReference()](../../com.aspose.words/list\#isListStyleReference--)将是真的。

列表可以是列表样式的定义，在这种情况下[isListStyleDefinition()](../../com.aspose.words/list\#isListStyleDefinition--)将是真的。这样的列表不能直接应用于文档中的段落。

**退货：**
[Style](../../com.aspose.words/style) - 此列表引用或定义的列表样式。
### hasSameTemplate(List other) {#hasSameTemplate-com.aspose.words.List-}
```
public boolean hasSameTemplate(List other)
```


如果当前列表和给定列表是从同一模板创建的，则返回 true。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| other | [List](../../com.aspose.words/list) |  |

**退货：**
布尔值
### hashCode() {#hashCode--}
```
public int hashCode()
```




**退货：**
整数
### isListStyleDefinition() {#isListStyleDefinition--}
```
public boolean isListStyleDefinition()
```


如果此列表是列表样式的定义，则返回 true。

当该属性为真时，[getStyle()](../../com.aspose.words/list\#getStyle--)属性返回此列表定义的列表样式。

通过修改定义列表样式的列表属性，您可以修改列表样式的属性。

作为列表样式定义的列表不能直接应用于段落以使它们编号。

**退货：**
boolean - 如果此列表是列表样式的定义，则为真。
### isListStyleReference() {#isListStyleReference--}
```
public boolean isListStyleReference()
```


如果此列表是对列表样式的引用，则返回 true。

请注意，修改引用列表样式的列表的属性无效。列表样式本身中指定的列表格式始终优先。

**退货：**
boolean - 如果此列表是对列表样式的引用，则为真。
### isMultiLevel() {#isMultiLevel--}
```
public boolean isMultiLevel()
```


当列表包含 9 个级别时返回 true； 1 级时为假。

您使用 Aspose.Words 创建的列表始终是多级列表，包含 9 个级别。

Microsoft Word 2003 及更高版本始终创建具有 9 个级别的多级列表。但在某些使用早期版本的 Microsoft Word 创建的文档中，您可能会遇到只有 1 级的列表。

**退货：**
boolean - 当列表包含 9 个级别时为真； 1 级时为假。
### isRestartAtEachSection() {#isRestartAtEachSection--}
```
public boolean isRestartAtEachSection()
```


指定是否应在每个部分重新启动列表。默认值为**false**.

此选项仅在 RTF、DOC 和 DOCX 文档格式中受支持。

只有在以下情况下，此选项才会写入 DOCX[OoxmlCompliance](../../com.aspose.words/ooxmlcompliance)高于[OoxmlCompliance.ECMA\_376\_2006](../../com.aspose.words/ooxmlcompliance\#ECMA-376-2006).

**退货：**
boolean - 相应的布尔值。
### isRestartAtEachSection(boolean value) {#isRestartAtEachSection-boolean-}
```
public void isRestartAtEachSection(boolean value)
```


指定是否应在每个部分重新启动列表。默认值为**false**.

此选项仅在 RTF、DOC 和 DOCX 文档格式中受支持。

只有在以下情况下，此选项才会写入 DOCX[OoxmlCompliance](../../com.aspose.words/ooxmlcompliance)高于[OoxmlCompliance.ECMA\_376\_2006](../../com.aspose.words/ooxmlcompliance\#ECMA-376-2006).

**参数：**

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




### toString() {#toString--}
```
public String toString()
```




**退货：**
java.lang.字符串
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
