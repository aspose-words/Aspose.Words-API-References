---
title: FieldTA
second_title: Aspose.Words for Java API 参考
description: 实现 TA 字段。
type: docs
weight: 249
url: /zh/java/com.aspose.words/fieldta/
---

**遗产：**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldTA extends Field
```

实现 TA 字段。

要了解更多信息，请访问**Working with Fields**文档文章。

为 TOA 字段使用的权限条目表定义文本和页码。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDisplayResult()](#getDisplayResult--) | 获取表示显示的字段结果的文本。 |
| [getEnd()](#getEnd--) | 获取表示字段结束的节点。 |
| [getEntryCategory()](#getEntryCategory--) | 获取整数条目类别，这是一个与类别顺序相对应的数字。 |
| [getFieldCode()](#getFieldCode--) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [getFormat()](#getFormat--) | 得到一个[FieldFormat](../../com.aspose.words/fieldformat)提供对字段格式的类型化访问的对象。 |
| [getLocaleId()](#getLocaleId--) | 获取字段的 LCID。 |
| [getLongCitation()](#getLongCitation--) | 获取条目的长引用。 |
| [getPageRangeBookmarkName()](#getPageRangeBookmarkName--) | 获取书签的名称，该书签将插入的页面范围标记为条目的页码。 |
| [getResult()](#getResult--) | 获取字段分隔符和字段结尾之间的文本。 |
| [getSeparator()](#getSeparator--) | 获取表示字段分隔符的节点。 |
| [getShortCitation()](#getShortCitation--) | 获取条目的简短引用。 |
| [getStart()](#getStart--) | 获取表示字段开始的节点。 |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getType()](#getType--) | 获取 Microsoft Word 字段类型。 |
| [hashCode()](#hashCode--) |  |
| [isBold()](#isBold--) | 获取是否对条目的页码应用粗体格式。 |
| [isBold(boolean value)](#isBold-boolean-) | 设置是否对条目的页码应用粗体格式。 |
| [isDirty()](#isDirty--) | 获取字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。 |
| [isDirty(boolean value)](#isDirty-boolean-) | 设置字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。 |
| [isItalic()](#isItalic--) | 获取是否对条目的页码应用斜体格式。 |
| [isItalic(boolean value)](#isItalic-boolean-) | 设置是否对条目的页码应用斜体格式。 |
| [isLocked()](#isLocked--) | 获取字段是否已锁定（不应重新计算其结果）。 |
| [isLocked(boolean value)](#isLocked-boolean-) | 设置字段是否被锁定（不应重新计算其结果）。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | 从文档中删除字段。 |
| [setEntryCategory(String value)](#setEntryCategory-java.lang.String-) | 设置整数条目类别，这是一个与类别顺序相对应的数字。 |
| [setLocaleId(int value)](#setLocaleId-int-) | 设置字段的 LCID。 |
| [setLongCitation(String value)](#setLongCitation-java.lang.String-) | 设置条目的长引用。 |
| [setPageRangeBookmarkName(String value)](#setPageRangeBookmarkName-java.lang.String-) | 设置书签的名称，该书签将插入的页面范围标记为条目的页码。 |
| [setResult(String value)](#setResult-java.lang.String-) | 设置字段分隔符和字段结尾之间的文本。 |
| [setShortCitation(String value)](#setShortCitation-java.lang.String-) | 设置条目的短引用。 |
| [toString()](#toString--) |  |
| [unlink()](#unlink--) | 执行字段取消链接。 |
| [update()](#update--) | 执行字段更新。 |
| [update(boolean ignoreMergeFormat)](#update-boolean-) | 执行字段更新。 |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货：**
布尔值
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getDisplayResult() {#getDisplayResult--}
```
public String getDisplayResult()
```


获取表示显示的字段结果的文本。这[Document.updateListLabels()](../../com.aspose.words/document\#updateListLabels--)必须调用方法以获得正确的值[FieldListNum](../../com.aspose.words/fieldlistnum), [FieldAutoNum](../../com.aspose.words/fieldautonum), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout)和[FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl)字段。

**退货：**
java.lang.String - 表示显示字段结果的文本。
### getEnd() {#getEnd--}
```
public FieldEnd getEnd()
```


获取表示字段结束的节点。

**退货：**
[FieldEnd](../../com.aspose.words/fieldend) - 表示字段结束的节点。
### getEntryCategory() {#getEntryCategory--}
```
public String getEntryCategory()
```


获取整数条目类别，这是一个与类别顺序相对应的数字。

**退货：**
java.lang.String - 整数条目类别，它是一个对应于类别顺序的数字。
### getFieldCode() {#getFieldCode--}
```
public String getFieldCode()
```


返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。包括子字段的字段代码和字段结果。

**退货：**
java.lang.字符串
### getFieldCode(boolean includeChildFieldCodes) {#getFieldCode-boolean-}
```
public String getFieldCode(boolean includeChildFieldCodes)
```


返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| includeChildFieldCodes | boolean | \{ 如果应包含子域代码则为真。 |

**退货：**
java.lang.字符串
### getFormat() {#getFormat--}
```
public FieldFormat getFormat()
```


得到一个[FieldFormat](../../com.aspose.words/fieldformat)提供对字段格式的类型化访问的对象。

**退货：**
[FieldFormat](../../com.aspose.words/fieldformat) - 一个[FieldFormat](../../com.aspose.words/fieldformat)提供对字段格式的类型化访问的对象。
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


获取字段的 LCID。

**退货：**
int - 字段的 LCID。
### getLongCitation() {#getLongCitation--}
```
public String getLongCitation()
```


获取条目的长引用。

**退货：**
java.lang.String - 条目的长引用。
### getPageRangeBookmarkName() {#getPageRangeBookmarkName--}
```
public String getPageRangeBookmarkName()
```


获取书签的名称，该书签将插入的页面范围标记为条目的页码。

**退货：**
java.lang.String - 标记作为条目页码插入的一系列页面的书签的名称。
### getResult() {#getResult--}
```
public String getResult()
```


获取字段分隔符和字段结尾之间的文本。

**退货：**
java.lang.String - 字段分隔符和字段结尾之间的文本。
### getSeparator() {#getSeparator--}
```
public FieldSeparator getSeparator()
```


获取表示字段分隔符的节点。可以为空。

**退货：**
[FieldSeparator](../../com.aspose.words/fieldseparator) - 表示字段分隔符的节点。
### getShortCitation() {#getShortCitation--}
```
public String getShortCitation()
```


获取条目的简短引用。

**退货：**
java.lang.String - 条目的简短引用。
### getStart() {#getStart--}
```
public FieldStart getStart()
```


获取表示字段开始的节点。

**退货：**
[FieldStart](../../com.aspose.words/fieldstart) - 表示字段开始的节点。
### getSwitchType(String switchName) {#getSwitchType-java.lang.String-}
```
public int getSwitchType(String switchName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| switchName | java.lang.String |  |

**退货：**
整数
### getType() {#getType--}
```
public int getType()
```


获取 Microsoft Word 字段类型。

**退货：**
 int - Microsoft Word 字段类型。返回值是其中之一[FieldType](../../com.aspose.words/fieldtype)常数。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### isBold() {#isBold--}
```
public boolean isBold()
```


获取是否对条目的页码应用粗体格式。

**退货：**
boolean - 是否对条目的页码应用粗体格式。
### isBold(boolean value) {#isBold-boolean-}
```
public void isBold(boolean value)
```


设置是否对条目的页码应用粗体格式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否对条目的页码应用粗体格式。 |

### isDirty() {#isDirty--}
```
public boolean isDirty()
```


获取字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。

**退货：**
布尔值 - 由于对文档进行的其他修改，该字段的当前结果是否不再正确（陈旧）。
### isDirty(boolean value) {#isDirty-boolean-}
```
public void isDirty(boolean value)
```


设置字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 由于对文档进行的其他修改，字段的当前结果是否不再正确（陈旧）。 |

### isItalic() {#isItalic--}
```
public boolean isItalic()
```


获取是否对条目的页码应用斜体格式。

**退货：**
boolean - 是否对条目的页码应用斜体格式。
### isItalic(boolean value) {#isItalic-boolean-}
```
public void isItalic(boolean value)
```


设置是否对条目的页码应用斜体格式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否对条目的页码应用斜体格式。 |

### isLocked() {#isLocked--}
```
public boolean isLocked()
```


获取字段是否已锁定（不应重新计算其结果）。

**退货：**
boolean - 该字段是否已锁定（不应重新计算其结果）。
### isLocked(boolean value) {#isLocked-boolean-}
```
public void isLocked(boolean value)
```


设置字段是否被锁定（不应重新计算其结果）。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 该字段是否已锁定（不应重新计算其结果）。 |

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
public Node remove()
```


从文档中删除字段。返回字段之后的节点。如果字段的末尾是其父节点的最后一个子节点，则返回其父段落。如果该字段已被删除，则返回**null**.

**退货：**
[Node](../../com.aspose.words/node)
### setEntryCategory(String value) {#setEntryCategory-java.lang.String-}
```
public void setEntryCategory(String value)
```


设置整数条目类别，这是一个与类别顺序相对应的数字。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 整数条目类别，这是一个与类别顺序相对应的数字。 |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


设置字段的 LCID。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 字段的 LCID。 |

### setLongCitation(String value) {#setLongCitation-java.lang.String-}
```
public void setLongCitation(String value)
```


设置条目的长引用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 条目的长引用。 |

### setPageRangeBookmarkName(String value) {#setPageRangeBookmarkName-java.lang.String-}
```
public void setPageRangeBookmarkName(String value)
```


设置书签的名称，该书签将插入的页面范围标记为条目的页码。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 标记作为条目页码插入的页面范围的书签的名称。 |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


设置字段分隔符和字段结尾之间的文本。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 字段分隔符和字段结尾之间的文本。 |

### setShortCitation(String value) {#setShortCitation-java.lang.String-}
```
public void setShortCitation(String value)
```


设置条目的短引用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 条目的简短引用。 |

### toString() {#toString--}
```
public String toString()
```




**退货：**
java.lang.字符串
### unlink() {#unlink--}
```
public boolean unlink()
```


执行字段取消链接。

用其最新结果替换该字段。

某些字段，例如 XE（索引条目）字段和 SEQ（序列）字段，无法取消链接。

**退货：**
布尔值 -\{ 如果字段已取消链接，则为真，否则为假。
### update() {#update--}
```
public void update()
```


执行字段更新。如果该字段已被更新，则抛出。

### update(boolean ignoreMergeFormat) {#update-boolean-}
```
public void update(boolean ignoreMergeFormat)
```


执行字段更新。如果该字段已被更新，则抛出。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ignoreMergeFormat | boolean | 如果为 true，则放弃直接字段结果格式化，无论 MERGEFORMAT 开关如何，否则执行正常更新。 |

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
