---
title: FieldToa
second_title: Aspose.Words for Java API 参考
description: 实现 TOA 字段。
type: docs
weight: 254
url: /zh/java/com.aspose.words/fieldtoa/
---

**遗产：**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldToa extends Field
```

实现 TOA 字段。

要了解更多信息，请访问**Working with Fields**文档文章。

使用 TA 字段指定的条目构建一个权限表（即法律文件中的引用列表，例如对案例、法规和规则的引用，以及引用出现的页码） .
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBookmarkName()](#getBookmarkName--) | 获取标记文档中用于构建表的部分的书签的名称。 |
| [getClass()](#getClass--) |  |
| [getDisplayResult()](#getDisplayResult--) | 获取表示显示的字段结果的文本。 |
| [getEnd()](#getEnd--) | 获取表示字段结束的节点。 |
| [getEntryCategory()](#getEntryCategory--) | 获取表中包含的条目的完整类别。 |
| [getEntrySeparator()](#getEntrySeparator--) | 获取用于分隔引文目录条目及其页码的字符序列。 |
| [getFieldCode()](#getFieldCode--) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [getFormat()](#getFormat--) | 得到一个[FieldFormat](../../com.aspose.words/fieldformat)提供对字段格式的类型化访问的对象。 |
| [getLocaleId()](#getLocaleId--) | 获取字段的 LCID。 |
| [getPageNumberListSeparator()](#getPageNumberListSeparator--) | 获取用于分隔页码列表中两个页码的字符序列。 |
| [getPageRangeSeparator()](#getPageRangeSeparator--) | 获取用于分隔页面范围的开始和结束的字符序列。 |
| [getRemoveEntryFormatting()](#getRemoveEntryFormatting--) | 获取是否从引文目录中的条目中删除文档中条目文本的格式。 |
| [getResult()](#getResult--) | 获取字段分隔符和字段结尾之间的文本。 |
| [getSeparator()](#getSeparator--) | 获取表示字段分隔符的节点。 |
| [getSequenceName()](#getSequenceName--) | 获取其编号包含在页码中的序列的名称。 |
| [getSequenceSeparator()](#getSequenceSeparator--) | 获取用于分隔序号和页码的字符序列。 |
| [getStart()](#getStart--) | 获取表示字段开始的节点。 |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getType()](#getType--) | 获取 Microsoft Word 字段类型。 |
| [getUseHeading()](#getUseHeading--) | 获取是否在引文目录中包含条目的类别标题。 |
| [getUsePassim()](#getUsePassim--) | 获取是否用“passim”替换对同一权威的五个或更多不同页面引用，用于表示某个词或段落在引用的作品中频繁出现。 |
| [hashCode()](#hashCode--) |  |
| [isDirty()](#isDirty--) | 获取字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。 |
| [isDirty(boolean value)](#isDirty-boolean-) | 设置字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。 |
| [isLocked()](#isLocked--) | 获取字段是否已锁定（不应重新计算其结果）。 |
| [isLocked(boolean value)](#isLocked-boolean-) | 设置字段是否被锁定（不应重新计算其结果）。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | 从文档中删除字段。 |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String-) | 设置标记用于构建表的文档部分的书签的名称。 |
| [setEntryCategory(String value)](#setEntryCategory-java.lang.String-) | 为表中包含的条目设置积分类别。 |
| [setEntrySeparator(String value)](#setEntrySeparator-java.lang.String-) | 设置用于分隔引文目录条目及其页码的字符序列。 |
| [setLocaleId(int value)](#setLocaleId-int-) | 设置字段的 LCID。 |
| [setPageNumberListSeparator(String value)](#setPageNumberListSeparator-java.lang.String-) | 设置用于分隔页码列表中两个页码的字符序列。 |
| [setPageRangeSeparator(String value)](#setPageRangeSeparator-java.lang.String-) | 设置用于分隔页面范围的开始和结束的字符序列。 |
| [setRemoveEntryFormatting(boolean value)](#setRemoveEntryFormatting-boolean-) | 设置是否从权限表中的条目中删除文档中条目文本的格式。 |
| [setResult(String value)](#setResult-java.lang.String-) | 设置字段分隔符和字段结尾之间的文本。 |
| [setSequenceName(String value)](#setSequenceName-java.lang.String-) | 设置其编号包含在页码中的序列的名称。 |
| [setSequenceSeparator(String value)](#setSequenceSeparator-java.lang.String-) | 设置用于分隔序号和页码的字符序列。 |
| [setUseHeading(boolean value)](#setUseHeading-boolean-) | 设置是否在权限表中包含条目的类别标题。 |
| [setUsePassim(boolean value)](#setUsePassim-boolean-) | 设置是否用“passim”替换对同一权威的五个或更多不同的页面引用，这用于指示一个单词或段落在被引用的作品中经常出现。 |
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


获取标记文档中用于构建表的部分的书签的名称。

**退货：**
java.lang.String - 标记用于构建表的文档部分的书签的名称。
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


获取表中包含的条目的完整类别。

**退货：**
java.lang.String - 表中包含的条目的整体类别。
### getEntrySeparator() {#getEntrySeparator--}
```
public String getEntrySeparator()
```


获取用于分隔引文目录条目及其页码的字符序列。

**退货：**
java.lang.String - 用于分隔权限表条目及其页码的字符序列。
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
### getPageNumberListSeparator() {#getPageNumberListSeparator--}
```
public String getPageNumberListSeparator()
```


获取用于分隔页码列表中两个页码的字符序列。

**退货：**
java.lang.String - 用于分隔页码列表中两个页码的字符序列。
### getPageRangeSeparator() {#getPageRangeSeparator--}
```
public String getPageRangeSeparator()
```


获取用于分隔页面范围的开始和结束的字符序列。

**退货：**
java.lang.String - 用于分隔页面范围的开始和结束的字符序列。
### getRemoveEntryFormatting() {#getRemoveEntryFormatting--}
```
public boolean getRemoveEntryFormatting()
```


获取是否从引文目录中的条目中删除文档中条目文本的格式。

**退货：**
boolean - 是否从权限表中的条目中删除文档中条目文本的格式。
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
### getSequenceName() {#getSequenceName--}
```
public String getSequenceName()
```


获取其编号包含在页码中的序列的名称。

**退货：**
java.lang.String - 序列的名称，其编号包含在页码中。
### getSequenceSeparator() {#getSequenceSeparator--}
```
public String getSequenceSeparator()
```


获取用于分隔序号和页码的字符序列。

**退货：**
java.lang.String - 用于分隔序列号和页码的字符序列。
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
### getUseHeading() {#getUseHeading--}
```
public boolean getUseHeading()
```


获取是否在引文目录中包含条目的类别标题。

**退货：**
boolean - 是否在权限表中包含条目的类别标题。
### getUsePassim() {#getUsePassim--}
```
public boolean getUsePassim()
```


获取是否用“passim”替换对同一权威的五个或更多不同页面引用，用于表示某个词或段落在引用的作品中频繁出现。

**退货：**
boolean - 是否将对同一权威的五个或更多不同页面引用替换为“passim”，用于表示某个词或段落在引用的作品中频繁出现。
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


设置标记用于构建表的文档部分的书签的名称。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 标记用于构建表的文档部分的书签的名称。 |

### setEntryCategory(String value) {#setEntryCategory-java.lang.String-}
```
public void setEntryCategory(String value)
```


为表中包含的条目设置积分类别。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 表中包含的条目的完整类别。 |

### setEntrySeparator(String value) {#setEntrySeparator-java.lang.String-}
```
public void setEntrySeparator(String value)
```


设置用于分隔引文目录条目及其页码的字符序列。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 用于分隔引文目录条目及其页码的字符序列。 |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


设置字段的 LCID。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 字段的 LCID。 |

### setPageNumberListSeparator(String value) {#setPageNumberListSeparator-java.lang.String-}
```
public void setPageNumberListSeparator(String value)
```


设置用于分隔页码列表中两个页码的字符序列。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 用于分隔页码列表中两个页码的字符序列。 |

### setPageRangeSeparator(String value) {#setPageRangeSeparator-java.lang.String-}
```
public void setPageRangeSeparator(String value)
```


设置用于分隔页面范围的开始和结束的字符序列。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 用于分隔页面范围的开始和结束的字符序列。 |

### setRemoveEntryFormatting(boolean value) {#setRemoveEntryFormatting-boolean-}
```
public void setRemoveEntryFormatting(boolean value)
```


设置是否从权限表中的条目中删除文档中条目文本的格式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否从引文目录中的条目中删除文档中条目文本的格式。 |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


设置字段分隔符和字段结尾之间的文本。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 字段分隔符和字段结尾之间的文本。 |

### setSequenceName(String value) {#setSequenceName-java.lang.String-}
```
public void setSequenceName(String value)
```


设置其编号包含在页码中的序列的名称。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 其编号包含在页码中的序列的名称。 |

### setSequenceSeparator(String value) {#setSequenceSeparator-java.lang.String-}
```
public void setSequenceSeparator(String value)
```


设置用于分隔序号和页码的字符序列。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 用于分隔序号和页码的字符序列。 |

### setUseHeading(boolean value) {#setUseHeading-boolean-}
```
public void setUseHeading(boolean value)
```


设置是否在权限表中包含条目的类别标题。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否在引文目录中包含条目的类别标题。 |

### setUsePassim(boolean value) {#setUsePassim-boolean-}
```
public void setUsePassim(boolean value)
```


设置是否用“passim”替换对同一权威的五个或更多不同的页面引用，这用于指示一个单词或段落在被引用的作品中经常出现。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否用“passim”替换同一权威的五个或更多不同页面引用，用于表示某个词或段落在所引用的作品中频繁出现。 |

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
