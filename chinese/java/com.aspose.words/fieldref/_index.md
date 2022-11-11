---
title: 字段Ref
second_title: Aspose.Words for Java API 参考
description:实现 REF 字段。
type: docs
weight: 235
url: /zh/java/com.aspose.words/fieldref/
---

**遗产:**
java.lang.Object, [com.aspose.words.字段](../../com.aspose.words/field)
```
public class 字段Ref extends 字段
```

实现 REF 字段。

要了解更多信息，请访问**Working with 字段**文档文章。

插入由指定书签表示的文本或图形。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [canWorkAsMerge字段()](#canWorkAsMerge字段--) |  |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBookmarkName()](#getBookmarkName--) | 获取引用书签的名称。 |
| [get班级()](#get班级--) |  |
| [getDisplayResult()](#getDisplayResult--) | 获取表示显示的字段结果的文本。 |
| [getEnd()](#getEnd--) | 获取表示字段结束的节点。 |
| [get字段Code()](#get字段Code--) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [get字段Code(boolean includeChild字段Codes)](#get字段Code-boolean-) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [getFormat()](#getFormat--) | 得到一个[字段Format](../../com.aspose.words/fieldformat)提供对字段格式的类型化访问的对象。 |
| [getIncludeNoteOrComment()](#getIncludeNoteOrComment--) | 获取是否增加书签标记的脚注、尾注和注释编号，并插入相应的脚注、尾注和注释文本。 |
| [getInsertHyperlink()](#getInsertHyperlink--) | 获取是否创建到书签段落的超链接。 |
| [getInsertParagraphNumber()](#getInsertParagraphNumber--) | 获取是否插入被引用段落的段落编号，与它在文档中出现的完全一样。 |
| [getInsertParagraphNumberInFullContext()](#getInsertParagraphNumberInFullContext--) | 获取是否在完整上下文中插入引用段落的段落编号。 |
| [getInsertParagraphNumberInRelativeContext()](#getInsertParagraphNumberInRelativeContext--) | 获取是否在相关上下文中插入被引用段落的段落编号。 |
| [getInsertRelativePosition()](#getInsertRelativePosition--) | 获取是否插入被引用段落的相对位置。 |
| [getLocaleId()](#getLocaleId--) | 获取字段的 LCID。 |
| [getMerge字段Name()](#getMerge字段Name--) |  |
| [getNumberSeparator()](#getNumberSeparator--) | 获取用于分隔序号和页码的字符序列。 |
| [getResult()](#getResult--) | 获取字段分隔符和字段结尾之间的文本。 |
| [getSeparator()](#getSeparator--) | 获取表示字段分隔符的节点。 |
| [getStart()](#getStart--) | 获取表示字段开始的节点。 |
| [getSuppressNonDelimiters()](#getSuppressNonDelimiters--) | 获取是否抑制非分隔符。 |
| [getSwitch类型(String switchName)](#getSwitch类型-java.lang.String-) |  |
| [get类型()](#get类型--) | 获取 Microsoft Word 字段类型。 |
| [hashCode()](#hashCode--) |  |
| [isDirty()](#isDirty--) | 获取字段的当前结果是否由于对文档进行了其他修改而不再正确（陈旧）。 |
| [isDirty(boolean value)](#isDirty-boolean-) | 设置字段的当前结果是否由于对文档的其他修改而不再正确（陈旧）。 |
| [isLocked()](#isLocked--) | 获取字段是否被锁定（不应重新计算其结果）。 |
| [isLocked(boolean value)](#isLocked-boolean-) | 设置字段是否被锁定（不应重新计算其结果）。 |
| [isMergeValueRequired()](#isMergeValueRequired--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | 从文档中删除字段。 |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String-) | 设置引用书签的名称。 |
| [setIncludeNoteOrComment(boolean value)](#setIncludeNoteOrComment-boolean-) | 设置是否增加书签标记的脚注、尾注和注释编号，并插入相应的脚注、尾注和注释文本。 |
| [setInsertHyperlink(boolean value)](#setInsertHyperlink-boolean-) | 设置是否创建到书签段落的超链接。 |
| [setInsertParagraphNumber(boolean value)](#setInsertParagraphNumber-boolean-) | 设置是否插入引用段落的段落编号，使其与文档中出现的完全相同。 |
| [setInsertParagraphNumberInFullContext(boolean value)](#setInsertParagraphNumberInFullContext-boolean-) | 设置是否在完整上下文中插入引用段落的段落编号。 |
| [setInsertParagraphNumberInRelativeContext(boolean value)](#setInsertParagraphNumberInRelativeContext-boolean-) | 设置是否在相关上下文中插入被引用段落的段落编号。 |
| [setInsertRelativePosition(boolean value)](#setInsertRelativePosition-boolean-) | 设置是否插入被引用段落的相对位置。 |
| [setLocaleId(int value)](#setLocaleId-int-) | 设置字段的 LCID。 |
| [setNumberSeparator(String value)](#setNumberSeparator-java.lang.String-) | 设置用于分隔序号和页码的字符序列。 |
| [setResult(String value)](#setResult-java.lang.String-) | 设置字段分隔符和字段结尾之间的文本。 |
| [setSuppressNonDelimiters(boolean value)](#setSuppressNonDelimiters-boolean-) | 设置是否禁止非分隔符。 |
| [toString()](#toString--) |  |
| [unlink()](#unlink--) | 执行字段取消链接。 |
| [update()](#update--) | 执行字段更新。 |
| [update(boolean ignoreMergeFormat)](#update-boolean-) | 执行字段更新。 |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### canWorkAsMerge字段() {#canWorkAsMerge字段--}
```
public boolean canWorkAsMerge字段()
```




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
### getBookmarkName() {#getBookmarkName--}
```
public String getBookmarkName()
```


获取引用书签的名称。

**退货:**
java.lang.String - 引用书签的名称。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getDisplayResult() {#getDisplayResult--}
```
public String getDisplayResult()
```


获取表示显示的字段结果的文本。这[Document.updateListLabels()](../../com.aspose.words/document\#updateListLabels--)必须调用方法才能获得正确的值[字段ListNum](../../com.aspose.words/fieldlistnum), [字段AutoNum](../../com.aspose.words/fieldautonum), [字段AutoNumOut](../../com.aspose.words/fieldautonumout)和[字段AutoNumLgl](../../com.aspose.words/fieldautonumlgl)字段。

**退货:**
java.lang.String - 表示显示的字段结果的文本。
### getEnd() {#getEnd--}
```
public 字段End getEnd()
```


获取表示字段结束的节点。

**退货:**
[字段End](../../com.aspose.words/fieldend) - 代表字段结束的节点。
### get字段Code() {#get字段Code--}
```
public String get字段Code()
```


返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。包含子字段的字段代码和字段结果。

**退货:**
java.lang.String
### get字段Code(boolean includeChild字段Codes) {#get字段Code-boolean-}
```
public String get字段Code(boolean includeChild字段Codes)
```


返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| includeChild字段Codes | boolean | \{ 如果应包含子域代码，则为真。 |

**退货:**
java.lang.String
### getFormat() {#getFormat--}
```
public 字段Format getFormat()
```


得到一个[字段Format](../../com.aspose.words/fieldformat)提供对字段格式的类型化访问的对象。

**退货:**
[字段Format](../../com.aspose.words/fieldformat) - 一个[字段Format](../../com.aspose.words/fieldformat)提供对字段格式的类型化访问的对象。
### getIncludeNoteOrComment() {#getIncludeNoteOrComment--}
```
public boolean getIncludeNoteOrComment()
```


获取是否增加书签标记的脚注、尾注和注释编号，并插入相应的脚注、尾注和注释文本。

**退货:**
boolean - 是否增加书签标记的脚注、尾注和注释编号，并插入相应的脚注、尾注和注释文本。
### getInsertHyperlink() {#getInsertHyperlink--}
```
public boolean getInsertHyperlink()
```


获取是否创建到书签段落的超链接。

**退货:**
boolean - 是否创建到书签段落的超链接。
### getInsertParagraphNumber() {#getInsertParagraphNumber--}
```
public boolean getInsertParagraphNumber()
```


获取是否插入被引用段落的段落编号，与它在文档中出现的完全一样。

**退货:**
boolean - 是否插入引用段落的段落编号，与文档中出现的完全相同。
### getInsertParagraphNumberInFullContext() {#getInsertParagraphNumberInFullContext--}
```
public boolean getInsertParagraphNumberInFullContext()
```


获取是否在完整上下文中插入引用段落的段落编号。

**退货:**
boolean - 是否在完整上下文中插入引用段落的段落编号。
### getInsertParagraphNumberInRelativeContext() {#getInsertParagraphNumberInRelativeContext--}
```
public boolean getInsertParagraphNumberInRelativeContext()
```


获取是否在相关上下文中插入被引用段落的段落编号。

**退货:**
boolean - 是否在相关上下文中插入引用段落的段落编号。
### getInsertRelativePosition() {#getInsertRelativePosition--}
```
public boolean getInsertRelativePosition()
```


获取是否插入被引用段落的相对位置。

**退货:**
boolean - 是否插入被引用段落的相对位置。
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


获取字段的 LCID。

**退货:**
int - 字段的 LCID。
### getMerge字段Name() {#getMerge字段Name--}
```
public String getMerge字段Name()
```




**退货:**
java.lang.String
### getNumberSeparator() {#getNumberSeparator--}
```
public String getNumberSeparator()
```


获取用于分隔序号和页码的字符序列。

**退货:**
java.lang.String - 用于分隔序列号和页码的字符序列。
### getResult() {#getResult--}
```
public String getResult()
```


获取字段分隔符和字段结尾之间的文本。

**退货:**
java.lang.String - 字段分隔符和字段结尾之间的文本。
### getSeparator() {#getSeparator--}
```
public 字段Separator getSeparator()
```


获取表示字段分隔符的节点。可以为空。

**退货:**
[字段Separator](../../com.aspose.words/fieldseparator) - 表示字段分隔符的节点。
### getStart() {#getStart--}
```
public 字段Start getStart()
```


获取表示字段开始的节点。

**退货:**
[字段Start](../../com.aspose.words/fieldstart) - 表示字段开始的节点。
### getSuppressNonDelimiters() {#getSuppressNonDelimiters--}
```
public boolean getSuppressNonDelimiters()
```


获取是否抑制非分隔符。

**退货:**
boolean - 是否抑制非分隔符。
### getSwitch类型(String switchName) {#getSwitch类型-java.lang.String-}
```
public int getSwitch类型(String switchName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| switchName | java.lang.String |  |

**退货:**
整数
### get类型() {#get类型--}
```
public int get类型()
```


获取 Microsoft Word 字段类型。

**退货:**
 int - Microsoft Word 字段类型。返回值是以下之一[字段类型](../../com.aspose.words/fieldtype)常数。
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

### isMergeValueRequired() {#isMergeValueRequired--}
```
public boolean isMergeValueRequired()
```




**退货:**
布尔值
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


设置引用书签的名称。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 引用书签的名称。 |

### setIncludeNoteOrComment(boolean value) {#setIncludeNoteOrComment-boolean-}
```
public void setIncludeNoteOrComment(boolean value)
```


设置是否增加书签标记的脚注、尾注和注释编号，并插入相应的脚注、尾注和注释文本。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否增加书签标记的脚注、尾注和注释编号，并插入相应的脚注、尾注和注释文本。 |

### setInsertHyperlink(boolean value) {#setInsertHyperlink-boolean-}
```
public void setInsertHyperlink(boolean value)
```


设置是否创建到书签段落的超链接。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否创建到书签段落的超链接。 |

### setInsertParagraphNumber(boolean value) {#setInsertParagraphNumber-boolean-}
```
public void setInsertParagraphNumber(boolean value)
```


设置是否插入引用段落的段落编号，使其与文档中出现的完全相同。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否插入引用段落的段落编号，与它在文档中出现的完全一样。 |

### setInsertParagraphNumberInFullContext(boolean value) {#setInsertParagraphNumberInFullContext-boolean-}
```
public void setInsertParagraphNumberInFullContext(boolean value)
```


设置是否在完整上下文中插入引用段落的段落编号。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否在完整上下文中插入引用段落的段落编号。 |

### setInsertParagraphNumberInRelativeContext(boolean value) {#setInsertParagraphNumberInRelativeContext-boolean-}
```
public void setInsertParagraphNumberInRelativeContext(boolean value)
```


设置是否在相关上下文中插入被引用段落的段落编号。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否在相对上下文中插入引用段落的段落编号。 |

### setInsertRelativePosition(boolean value) {#setInsertRelativePosition-boolean-}
```
public void setInsertRelativePosition(boolean value)
```


设置是否插入被引用段落的相对位置。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否插入被引用段落的相对位置。 |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


设置字段的 LCID。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 字段的 LCID。 |

### setNumberSeparator(String value) {#setNumberSeparator-java.lang.String-}
```
public void setNumberSeparator(String value)
```


设置用于分隔序号和页码的字符序列。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 用于分隔序号和页码的字符序列。 |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


设置字段分隔符和字段结尾之间的文本。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 字段分隔符和字段结尾之间的文本。 |

### setSuppressNonDelimiters(boolean value) {#setSuppressNonDelimiters-boolean-}
```
public void setSuppressNonDelimiters(boolean value)
```


设置是否禁止非分隔符。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否抑制非定界字符。 |

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

用其最新结果替换该字段。

某些字段，例如 XE（索引条目）字段和 SEQ（序列）字段，无法取消链接。

**退货:**
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

**参数:**
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