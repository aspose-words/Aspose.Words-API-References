---
title: FieldSeq
second_title: Aspose.Words for Java API 参考
description: 实现 SEQ 字段。
type: docs
weight: 241
url: /zh/java/com.aspose.words/fieldseq/
---

**遗产：**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldSeq extends Field
```

实现 SEQ 字段。

要了解更多信息，请访问**Working with Fields**文档文章。

按顺序对文档中的章节、表格、图形和其他用户定义的项目列表进行编号。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBookmarkName()](#getBookmarkName--) | 获取一个书签名称，该名称引用文档中其他位置而不是当前位置的项目。 |
| [getClass()](#getClass--) |  |
| [getDisplayResult()](#getDisplayResult--) | 获取表示显示的字段结果的文本。 |
| [getEnd()](#getEnd--) | 获取表示字段结束的节点。 |
| [getFieldCode()](#getFieldCode--) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [getFormat()](#getFormat--) | 得到一个[FieldFormat](../../com.aspose.words/fieldformat)提供对字段格式的类型化访问的对象。 |
| [getInsertNextNumber()](#getInsertNextNumber--) | 获取是否为指定项插入下一个序号。 |
| [getLocaleId()](#getLocaleId--) | 获取字段的 LCID。 |
| [getResetHeadingLevel()](#getResetHeadingLevel--) | 获取一个整数，表示要将序列号重置为的标题级别。 |
| [getResetNumber()](#getResetNumber--) | 获取一个整数以将序列号重置为。 |
| [getResult()](#getResult--) | 获取字段分隔符和字段结尾之间的文本。 |
| [getSeparator()](#getSeparator--) | 获取表示字段分隔符的节点。 |
| [getSequenceIdentifier()](#getSequenceIdentifier--) | 获取分配给要编号的项目系列的名称。 |
| [getStart()](#getStart--) | 获取表示字段开始的节点。 |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getType()](#getType--) | 获取 Microsoft Word 字段类型。 |
| [hashCode()](#hashCode--) |  |
| [isDirty()](#isDirty--) | 获取字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。 |
| [isDirty(boolean value)](#isDirty-boolean-) | 设置字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。 |
| [isLocked()](#isLocked--) | 获取字段是否已锁定（不应重新计算其结果）。 |
| [isLocked(boolean value)](#isLocked-boolean-) | 设置字段是否被锁定（不应重新计算其结果）。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | 从文档中删除字段。 |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String-) | 设置一个书签名称，该名称引用文档中其他位置而不是当前位置的项目。 |
| [setInsertNextNumber(boolean value)](#setInsertNextNumber-boolean-) | 设置是否为指定项插入下一个序号。 |
| [setLocaleId(int value)](#setLocaleId-int-) | 设置字段的 LCID。 |
| [setResetHeadingLevel(String value)](#setResetHeadingLevel-java.lang.String-) | 设置一个整数，表示要将序列号重置为的标题级别。 |
| [setResetNumber(String value)](#setResetNumber-java.lang.String-) | 设置一个整数以将序列号重置为。 |
| [setResult(String value)](#setResult-java.lang.String-) | 设置字段分隔符和字段结尾之间的文本。 |
| [setSequenceIdentifier(String value)](#setSequenceIdentifier-java.lang.String-) | 设置分配给要编号的项目系列的名称。 |
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
### getBookmarkName() {#getBookmarkName--}
```
public String getBookmarkName()
```


获取一个书签名称，该名称引用文档中其他位置而不是当前位置的项目。

**退货：**
java.lang.String - 一个书签名称，它指的是文档中其他地方而不是当前位置的项目。
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
### getInsertNextNumber() {#getInsertNextNumber--}
```
public boolean getInsertNextNumber()
```


获取是否为指定项插入下一个序号。

**退货：**
boolean - 是否为指定项目插入下一个序列号。
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


获取字段的 LCID。

**退货：**
int - 字段的 LCID。
### getResetHeadingLevel() {#getResetHeadingLevel--}
```
public String getResetHeadingLevel()
```


获取一个整数，表示要将序列号重置为的标题级别。如果数字不存在，则返回 -1。

**退货：**
java.lang.String - 一个整数，表示要将序列号重置为的标题级别。
### getResetNumber() {#getResetNumber--}
```
public String getResetNumber()
```


获取一个整数以将序列号重置为。如果数字不存在，则返回 -1。

**退货：**
java.lang.String - 将序列号重置为的整数。
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
### getSequenceIdentifier() {#getSequenceIdentifier--}
```
public String getSequenceIdentifier()
```


获取分配给要编号的项目系列的名称。

**退货：**
java.lang.String - 分配给要编号的项目系列的名称。
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
### setBookmarkName(String value) {#setBookmarkName-java.lang.String-}
```
public void setBookmarkName(String value)
```


设置一个书签名称，该名称引用文档中其他位置而不是当前位置的项目。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 引用文档中其他位置而非当前位置的项目的书签名称。 |

### setInsertNextNumber(boolean value) {#setInsertNextNumber-boolean-}
```
public void setInsertNextNumber(boolean value)
```


设置是否为指定项插入下一个序号。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否为指定项目插入下一个序号。 |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


设置字段的 LCID。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 字段的 LCID。 |

### setResetHeadingLevel(String value) {#setResetHeadingLevel-java.lang.String-}
```
public void setResetHeadingLevel(String value)
```


设置一个整数，表示要将序列号重置为的标题级别。如果数字不存在，则返回 -1。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 一个整数，表示要将序列号重置为的标题级别。 |

### setResetNumber(String value) {#setResetNumber-java.lang.String-}
```
public void setResetNumber(String value)
```


设置一个整数以将序列号重置为。如果数字不存在，则返回 -1。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 将序列号重置为的整数。 |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


设置字段分隔符和字段结尾之间的文本。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 字段分隔符和字段结尾之间的文本。 |

### setSequenceIdentifier(String value) {#setSequenceIdentifier-java.lang.String-}
```
public void setSequenceIdentifier(String value)
```


设置分配给要编号的项目系列的名称。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 分配给要编号的项目系列的名称。 |

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
