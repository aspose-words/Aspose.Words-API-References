---
title: FieldTC
second_title: Aspose.Words for Java API 参考
description: 实现 TC 字段。
type: docs
weight: 250
url: /zh/java/com.aspose.words/fieldtc/
---

**遗产：**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldTC extends Field
```

实现 TC 字段。

要了解更多信息，请访问**Working with Fields**文档文章。

定义目录（包括图表）条目的文本和页码，由 TOC 字段使用。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDisplayResult()](#getDisplayResult--) | 获取表示显示的字段结果的文本。 |
| [getDocumentOutlineTitle()](#getDocumentOutlineTitle--) |  |
| [getEnd()](#getEnd--) | 获取表示字段结束的节点。 |
| [getEntryLevel()](#getEntryLevel--) | 获取条目的级别。 |
| [getFieldCode()](#getFieldCode--) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [getFormat()](#getFormat--) | 得到一个[FieldFormat](../../com.aspose.words/fieldformat)提供对字段格式的类型化访问的对象。 |
| [getLevel()](#getLevel--) |  |
| [getLocaleId()](#getLocaleId--) | 获取字段的 LCID。 |
| [getOmitPageNumber()](#getOmitPageNumber--) | 获取是否应为此字段省略 TOC 中的页码。 |
| [getPageNumber()](#getPageNumber--) |  |
| [getParagraph()](#getParagraph--) |  |
| [getResult()](#getResult--) | 获取字段分隔符和字段结尾之间的文本。 |
| [getSeparator()](#getSeparator--) | 获取表示字段分隔符的节点。 |
| [getSequenceValue(String sequenceIdentifier)](#getSequenceValue-java.lang.String-) |  |
| [getStart()](#getStart--) | 获取表示字段开始的节点。 |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getText()](#getText--) | 获取条目的文本。 |
| [getType()](#getType--) | 获取 Microsoft Word 字段类型。 |
| [getTypeIdentifier()](#getTypeIdentifier--) | 获取此字段的类型标识符（通常是字母）。 |
| [hasBookmark()](#hasBookmark--) |  |
| [hashCode()](#hashCode--) |  |
| [isDirty()](#isDirty--) | 获取字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。 |
| [isDirty(boolean value)](#isDirty-boolean-) | 设置字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。 |
| [isInFieldCode()](#isInFieldCode--) |  |
| [isLocked()](#isLocked--) | 获取字段是否已锁定（不应重新计算其结果）。 |
| [isLocked(boolean value)](#isLocked-boolean-) | 设置字段是否被锁定（不应重新计算其结果）。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | 从文档中删除字段。 |
| [setEntryLevel(String value)](#setEntryLevel-java.lang.String-) | 设置条目的级别。 |
| [setLocaleId(int value)](#setLocaleId-int-) | 设置字段的 LCID。 |
| [setOmitPageNumber(boolean value)](#setOmitPageNumber-boolean-) | 设置是否应为此字段省略 TOC 中的页码。 |
| [setResult(String value)](#setResult-java.lang.String-) | 设置字段分隔符和字段结尾之间的文本。 |
| [setText(String value)](#setText-java.lang.String-) | 设置条目的文本。 |
| [setTypeIdentifier(String value)](#setTypeIdentifier-java.lang.String-) | 为此字段设置类型标识符（通常是字母）。 |
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
### getDocumentOutlineTitle() {#getDocumentOutlineTitle--}
```
public String getDocumentOutlineTitle()
```




**退货：**
java.lang.字符串
### getEnd() {#getEnd--}
```
public FieldEnd getEnd()
```


获取表示字段结束的节点。

**退货：**
[FieldEnd](../../com.aspose.words/fieldend) - 表示字段结束的节点。
### getEntryLevel() {#getEntryLevel--}
```
public String getEntryLevel()
```


获取条目的级别。

**退货：**
java.lang.String - 条目的级别。
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
### getLevel() {#getLevel--}
```
public int getLevel()
```




**退货：**
整数
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


获取字段的 LCID。

**退货：**
int - 字段的 LCID。
### getOmitPageNumber() {#getOmitPageNumber--}
```
public boolean getOmitPageNumber()
```


获取是否应为此字段省略 TOC 中的页码。

**退货：**
布尔值 - 是否应为此字段省略 TOC 中的页码。
### getPageNumber() {#getPageNumber--}
```
public int getPageNumber()
```




**退货：**
整数
### getParagraph() {#getParagraph--}
```
public Paragraph getParagraph()
```




**退货：**
[Paragraph](../../com.aspose.words/paragraph)
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
### getSequenceValue(String sequenceIdentifier) {#getSequenceValue-java.lang.String-}
```
public int getSequenceValue(String sequenceIdentifier)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sequenceIdentifier | java.lang.String |  |

**退货：**
整数
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
### getText() {#getText--}
```
public String getText()
```


获取条目的文本。

**退货：**
java.lang.String - 条目的文本。
### getType() {#getType--}
```
public int getType()
```


获取 Microsoft Word 字段类型。

**退货：**
 int - Microsoft Word 字段类型。返回值是其中之一[FieldType](../../com.aspose.words/fieldtype)常数。
### getTypeIdentifier() {#getTypeIdentifier--}
```
public String getTypeIdentifier()
```


获取此字段的类型标识符（通常是字母）。

**退货：**
java.lang.String - 此字段的类型标识符（通常是字母）。
### hasBookmark() {#hasBookmark--}
```
public boolean hasBookmark()
```




**退货：**
布尔值
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
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

### isInFieldCode() {#isInFieldCode--}
```
public boolean isInFieldCode()
```




**退货：**
布尔值
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
### setEntryLevel(String value) {#setEntryLevel-java.lang.String-}
```
public void setEntryLevel(String value)
```


设置条目的级别。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 条目的级别。 |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


设置字段的 LCID。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 字段的 LCID。 |

### setOmitPageNumber(boolean value) {#setOmitPageNumber-boolean-}
```
public void setOmitPageNumber(boolean value)
```


设置是否应为此字段省略 TOC 中的页码。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 此字段是否应省略 TOC 中的页码。 |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


设置字段分隔符和字段结尾之间的文本。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 字段分隔符和字段结尾之间的文本。 |

### setText(String value) {#setText-java.lang.String-}
```
public void setText(String value)
```


设置条目的文本。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 条目的文本。 |

### setTypeIdentifier(String value) {#setTypeIdentifier-java.lang.String-}
```
public void setTypeIdentifier(String value)
```


为此字段设置类型标识符（通常是字母）。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 此字段的类型标识符（通常是字母）。 |

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
