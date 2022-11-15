---
title: FieldIndex
second_title: Aspose.Words for Java API 参考
description: 实现 INDEX 字段。
type: docs
weight: 206
url: /zh/java/com.aspose.words/fieldindex/
---

**遗产:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldIndex extends Field
```

实现 INDEX 字段。

要了解更多信息，请访问**Working with 字段**文档文章。

使用 XE 字段指定的索引条目构建索引，并将该索引插入文档中的此位置。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBookmarkName()](#getBookmarkName--) | 获取标记文档中用于构建索引的部分的书签名称。 |
| [getClass()](#getClass--) |  |
| [getCrossReferenceSeparator()](#getCrossReferenceSeparator--) | 获取用于分隔交叉引用和其他条目的字符序列。 |
| [getDisplayResult()](#getDisplayResult--) | 获取表示显示的字段结果的文本。 |
| [getEnd()](#getEnd--) | 获取表示字段结束的节点。 |
| [getEntryType()](#getEntryType--) | 获取用于构建索引的索引条目类型。 |
| [getFieldCode()](#getFieldCode--) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [getFormat()](#getFormat--) | 得到一个[FieldFormat](../../com.aspose.words/fieldformat)提供对字段格式的类型化访问的对象。 |
| [getHeading()](#getHeading--) | 获取出现在任何给定字母的每组条目开头的标题。 |
| [getLanguageId()](#getLanguageId--) | 获取用于生成索引的语言 ID。 |
| [getLetterRange()](#getLetterRange--) | 获取限制索引的字母范围。 |
| [getLocaleId()](#getLocaleId--) | 获取字段的 LCID。 |
| [getNumberOfColumns()](#getNumberOfColumns--) | 获取构建索引时每页使用的列数。 |
| [getPageNumberListSeparator()](#getPageNumberListSeparator--) | 获取用于分隔页码列表中两个页码的字符序列。 |
| [getPageNumberSeparator()](#getPageNumberSeparator--) | 获取用于分隔索引条目及其页码的字符序列。 |
| [getPageRangeSeparator()](#getPageRangeSeparator--) | 获取用于分隔页面范围的开始和结束的字符序列。 |
| [getResult()](#getResult--) | 获取字段分隔符和字段结尾之间的文本。 |
| [getRunSubentriesOnSameLine()](#getRunSubentriesOnSameLine--) | 获取是否将子条目运行到与主条目相同的行中。 |
| [getSeparator()](#getSeparator--) | 获取表示字段分隔符的节点。 |
| [getSequenceName()](#getSequenceName--) | 获取其编号包含在页码中的序列的名称。 |
| [getSequenceSeparator()](#getSequenceSeparator--) | 获取用于分隔序号和页码的字符序列。 |
| [getStart()](#getStart--) | 获取表示字段开始的节点。 |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getType()](#getType--) | 获取 Microsoft Word 字段类型。 |
| [getUseYomi()](#getUseYomi--) | 获取是否启用对索引条目使用 yomi 文本。 |
| [hasPageNumberSeparator()](#hasPageNumberSeparator--) | 获取一个值，该值指示页码分隔符是否被字段的代码覆盖。 |
| [hasSequenceName()](#hasSequenceName--) | 获取一个值，该值指示在构建字段的结果时是否应使用序列。 |
| [hashCode()](#hashCode--) |  |
| [isDirty()](#isDirty--) | 获取字段的当前结果是否由于对文档进行了其他修改而不再正确（陈旧）。 |
| [isDirty(boolean value)](#isDirty-boolean-) | 设置字段的当前结果是否由于对文档的其他修改而不再正确（陈旧）。 |
| [isLocked()](#isLocked--) | 获取字段是否被锁定（不应重新计算其结果）。 |
| [isLocked(boolean value)](#isLocked-boolean-) | 设置字段是否被锁定（不应重新计算其结果）。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | 从文档中删除字段。 |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String-) | 设置标记文档中用于构建索引的部分的书签名称。 |
| [setCrossReferenceSeparator(String value)](#setCrossReferenceSeparator-java.lang.String-) | 设置用于分隔交叉引用和其他条目的字符序列。 |
| [setEntryType(String value)](#setEntryType-java.lang.String-) | 设置用于构建索引的索引条目类型。 |
| [setHeading(String value)](#setHeading-java.lang.String-) | 为任何给定字母设置一个标题，该标题出现在每组条目的开头。 |
| [setLanguageId(String value)](#setLanguageId-java.lang.String-) | 设置用于生成索引的语言 ID。 |
| [setLetterRange(String value)](#setLetterRange-java.lang.String-) | 设置限制索引的字母范围。 |
| [setLocaleId(int value)](#setLocaleId-int-) | 设置字段的 LCID。 |
| [setNumberOfColumns(String value)](#setNumberOfColumns-java.lang.String-) | 设置构建索引时使用的每页列数。 |
| [setPageNumberListSeparator(String value)](#setPageNumberListSeparator-java.lang.String-) | 设置用于分隔页码列表中两个页码的字符序列。 |
| [setPageNumberSeparator(String value)](#setPageNumberSeparator-java.lang.String-) | 设置用于分隔索引条目及其页码的字符序列。 |
| [setPageRangeSeparator(String value)](#setPageRangeSeparator-java.lang.String-) | 设置用于分隔页面范围的开始和结束的字符序列。 |
| [setResult(String value)](#setResult-java.lang.String-) | 设置字段分隔符和字段结尾之间的文本。 |
| [setRunSubentriesOnSameLine(boolean value)](#setRunSubentriesOnSameLine-boolean-) | 设置是否将子条目运行到与主条目相同的行中。 |
| [setSequenceName(String value)](#setSequenceName-java.lang.String-) | 设置其编号包含在页码中的序列的名称。 |
| [setSequenceSeparator(String value)](#setSequenceSeparator-java.lang.String-) | 设置用于分隔序号和页码的字符序列。 |
| [setUseYomi(boolean value)](#setUseYomi-boolean-) | 设置是否为索引条目启用 yomi 文本。 |
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




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### getBookmarkName() {#getBookmarkName--}
```
public String getBookmarkName()
```


获取标记文档中用于构建索引的部分的书签名称。

**退货:**
java.lang.String - 标记用于构建索引的文档部分的书签的名称。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getCrossReferenceSeparator() {#getCrossReferenceSeparator--}
```
public String getCrossReferenceSeparator()
```


获取用于分隔交叉引用和其他条目的字符序列。

**退货:**
java.lang.String - 用于分隔交叉引用和其他条目的字符序列。
### getDisplayResult() {#getDisplayResult--}
```
public String getDisplayResult()
```


获取表示显示的字段结果的文本。这[Document.updateListLabels()](../../com.aspose.words/document\#updateListLabels--)必须调用方法才能获得正确的值[FieldListNum](../../com.aspose.words/fieldlistnum), [FieldAutoNum](../../com.aspose.words/fieldautonum), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout)和[FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl)字段。

**退货:**
java.lang.String - 表示显示的字段结果的文本。
### getEnd() {#getEnd--}
```
public FieldEnd getEnd()
```


获取表示字段结束的节点。

**退货:**
[FieldEnd](../../com.aspose.words/fieldend) - 代表字段结束的节点。
### getEntryType() {#getEntryType--}
```
public String getEntryType()
```


获取用于构建索引的索引条目类型。

**退货:**
java.lang.String - 用于构建索引的索引条目类型。
### getFieldCode() {#getFieldCode--}
```
public String getFieldCode()
```


返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。包含子字段的字段代码和字段结果。

**退货:**
java.lang.String
### getFieldCode(boolean includeChildFieldCodes) {#getFieldCode-boolean-}
```
public String getFieldCode(boolean includeChildFieldCodes)
```


返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| includeChildFieldCodes | boolean | \{ 如果应包含子域代码，则为真。 |

**退货:**
java.lang.String
### getFormat() {#getFormat--}
```
public FieldFormat getFormat()
```


得到一个[FieldFormat](../../com.aspose.words/fieldformat)提供对字段格式的类型化访问的对象。

**退货:**
[FieldFormat](../../com.aspose.words/fieldformat) - 一个[FieldFormat](../../com.aspose.words/fieldformat)提供对字段格式的类型化访问的对象。
### getHeading() {#getHeading--}
```
public String getHeading()
```


获取出现在任何给定字母的每组条目开头的标题。

**退货:**
java.lang.String - 出现在任何给定字母的每组条目开头的标题。
### getLanguageId() {#getLanguageId--}
```
public String getLanguageId()
```


获取用于生成索引的语言 ID。

**退货:**
java.lang.String - 用于生成索引的语言 ID。
### getLetterRange() {#getLetterRange--}
```
public String getLetterRange()
```


获取限制索引的字母范围。

**退货:**
java.lang.String - 限制索引的字母范围。
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


获取字段的 LCID。

**退货:**
int - 字段的 LCID。
### getNumberOfColumns() {#getNumberOfColumns--}
```
public String getNumberOfColumns()
```


获取构建索引时每页使用的列数。

**退货:**
java.lang.String - 构建索引时每页使用的列数。
### getPageNumberListSeparator() {#getPageNumberListSeparator--}
```
public String getPageNumberListSeparator()
```


获取用于分隔页码列表中两个页码的字符序列。

**退货:**
java.lang.String - 用于分隔页码列表中两个页码的字符序列。
### getPageNumberSeparator() {#getPageNumberSeparator--}
```
public String getPageNumberSeparator()
```


获取用于分隔索引条目及其页码的字符序列。

**退货:**
java.lang.String - 用于分隔索引条目及其页码的字符序列。
### getPageRangeSeparator() {#getPageRangeSeparator--}
```
public String getPageRangeSeparator()
```


获取用于分隔页面范围的开始和结束的字符序列。

**退货:**
java.lang.String - 用于分隔页面范围的开始和结束的字符序列。
### getResult() {#getResult--}
```
public String getResult()
```


获取字段分隔符和字段结尾之间的文本。

**退货:**
java.lang.String - 字段分隔符和字段结尾之间的文本。
### getRunSubentriesOnSameLine() {#getRunSubentriesOnSameLine--}
```
public boolean getRunSubentriesOnSameLine()
```


获取是否将子条目运行到与主条目相同的行中。

**退货:**
boolean - 是否将子条目运行到与主条目相同的行中。
### getSeparator() {#getSeparator--}
```
public FieldSeparator getSeparator()
```


获取表示字段分隔符的节点。可以为空。

**退货:**
[FieldSeparator](../../com.aspose.words/fieldseparator) - 表示字段分隔符的节点。
### getSequenceName() {#getSequenceName--}
```
public String getSequenceName()
```


获取其编号包含在页码中的序列的名称。

**退货:**
java.lang.String - 序列的名称，其编号包含在页码中。
### getSequenceSeparator() {#getSequenceSeparator--}
```
public String getSequenceSeparator()
```


获取用于分隔序号和页码的字符序列。

**退货:**
java.lang.String - 用于分隔序列号和页码的字符序列。
### getStart() {#getStart--}
```
public FieldStart getStart()
```


获取表示字段开始的节点。

**退货:**
[FieldStart](../../com.aspose.words/fieldstart) - 表示字段开始的节点。
### getSwitchType(String switchName) {#getSwitchType-java.lang.String-}
```
public int getSwitchType(String switchName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| switchName | java.lang.String |  |

**退货:**
整数
### getType() {#getType--}
```
public int getType()
```


获取 Microsoft Word 字段类型。

**退货:**
 int - Microsoft Word 字段类型。返回值是以下之一[FieldType](../../com.aspose.words/fieldtype)常数。
### getUseYomi() {#getUseYomi--}
```
public boolean getUseYomi()
```


获取是否启用对索引条目使用 yomi 文本。

**退货:**
boolean - 是否为索引条目启用 yomi 文本。
### hasPageNumberSeparator() {#hasPageNumberSeparator--}
```
public boolean hasPageNumberSeparator()
```


获取一个值，该值指示页码分隔符是否被字段的代码覆盖。

**退货:**
boolean - 一个值，指示是否通过字段的代码覆盖页码分隔符。
### hasSequenceName() {#hasSequenceName--}
```
public boolean hasSequenceName()
```


获取一个值，该值指示在构建字段的结果时是否应使用序列。

**退货:**
boolean - 一个值，指示在构建字段的结果时是否应使用序列。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isDirty() {#isDirty--}
```
public boolean isDirty()
```


获取字段的当前结果是否由于对文档进行了其他修改而不再正确（陈旧）。

**退货:**
boolean - 由于对文档进行了其他修改，该字段的当前结果是否不再正确（陈旧）。
### isDirty(boolean value) {#isDirty-boolean-}
```
public void isDirty(boolean value)
```


设置字段的当前结果是否由于对文档的其他修改而不再正确（陈旧）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 由于对文档进行了其他修改，该字段的当前结果是否不再正确（陈旧）。 |

### isLocked() {#isLocked--}
```
public boolean isLocked()
```


获取字段是否被锁定（不应重新计算其结果）。

**退货:**
boolean - 字段是否被锁定（不应重新计算其结果）。
### isLocked(boolean value) {#isLocked-boolean-}
```
public void isLocked(boolean value)
```


设置字段是否被锁定（不应重新计算其结果）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 该字段是否被锁定（不应重新计算其结果）。 |

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


从文档中删除字段。在字段之后返回一个节点。如果字段的结尾是其父节点的最后一个子节点，则返回其父段落。如果该字段已被删除，则返回**null**.

**退货:**
[Node](../../com.aspose.words/node)
### setBookmarkName(String value) {#setBookmarkName-java.lang.String-}
```
public void setBookmarkName(String value)
```


设置标记文档中用于构建索引的部分的书签名称。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 标记用于构建索引的文档部分的书签名称。 |

### setCrossReferenceSeparator(String value) {#setCrossReferenceSeparator-java.lang.String-}
```
public void setCrossReferenceSeparator(String value)
```


设置用于分隔交叉引用和其他条目的字符序列。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 用于分隔交叉引用和其他条目的字符序列。 |

### setEntryType(String value) {#setEntryType-java.lang.String-}
```
public void setEntryType(String value)
```


设置用于构建索引的索引条目类型。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 用于构建索引的索引条目类型。 |

### setHeading(String value) {#setHeading-java.lang.String-}
```
public void setHeading(String value)
```


为任何给定字母设置一个标题，该标题出现在每组条目的开头。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 出现在任何给定字母的每组条目开头的标题。 |

### setLanguageId(String value) {#setLanguageId-java.lang.String-}
```
public void setLanguageId(String value)
```


设置用于生成索引的语言 ID。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 用于生成索引的语言 ID。 |

### setLetterRange(String value) {#setLetterRange-java.lang.String-}
```
public void setLetterRange(String value)
```


设置限制索引的字母范围。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 限制索引的字母范围。 |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


设置字段的 LCID。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 字段的 LCID。 |

### setNumberOfColumns(String value) {#setNumberOfColumns-java.lang.String-}
```
public void setNumberOfColumns(String value)
```


设置构建索引时使用的每页列数。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 构建索引时每页使用的列数。 |

### setPageNumberListSeparator(String value) {#setPageNumberListSeparator-java.lang.String-}
```
public void setPageNumberListSeparator(String value)
```


设置用于分隔页码列表中两个页码的字符序列。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 用于分隔页码列表中两个页码的字符序列。 |

### setPageNumberSeparator(String value) {#setPageNumberSeparator-java.lang.String-}
```
public void setPageNumberSeparator(String value)
```


设置用于分隔索引条目及其页码的字符序列。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 用于分隔索引条目及其页码的字符序列。 |

### setPageRangeSeparator(String value) {#setPageRangeSeparator-java.lang.String-}
```
public void setPageRangeSeparator(String value)
```


设置用于分隔页面范围的开始和结束的字符序列。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 用于分隔页面范围的开始和结束的字符序列。 |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


设置字段分隔符和字段结尾之间的文本。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 字段分隔符和字段结尾之间的文本。 |

### setRunSubentriesOnSameLine(boolean value) {#setRunSubentriesOnSameLine-boolean-}
```
public void setRunSubentriesOnSameLine(boolean value)
```


设置是否将子条目运行到与主条目相同的行中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否将子条目运行到与主条目相同的行中。 |

### setSequenceName(String value) {#setSequenceName-java.lang.String-}
```
public void setSequenceName(String value)
```


设置其编号包含在页码中的序列的名称。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 编号包含在页码中的序列的名称。 |

### setSequenceSeparator(String value) {#setSequenceSeparator-java.lang.String-}
```
public void setSequenceSeparator(String value)
```


设置用于分隔序号和页码的字符序列。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 用于分隔序号和页码的字符序列。 |

### setUseYomi(boolean value) {#setUseYomi-boolean-}
```
public void setUseYomi(boolean value)
```


设置是否为索引条目启用 yomi 文本。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否为索引条目启用 yomi 文本。 |

### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### unlink() {#unlink--}
```
public boolean unlink()
```


执行字段取消链接。

将字段替换为其最新结果。

某些字段，例如 XE（索引条目）字段和 SEQ（序列）字段，无法取消链接。

**退货:**
布尔值 -\{ 如果该字段已取消链接则为真，否则为假。
### update() {#update--}
```
public void update()
```


执行字段更新。如果该字段已经被更新则抛出。

### update(boolean ignoreMergeFormat) {#update-boolean-}
```
public void update(boolean ignoreMergeFormat)
```


执行字段更新。如果该字段已经被更新则抛出。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ignoreMergeFormat | boolean | 如果为真，则放弃直接字段结果格式，不管 MERGEFORMAT 开关如何，否则执行正常更新。 |

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
