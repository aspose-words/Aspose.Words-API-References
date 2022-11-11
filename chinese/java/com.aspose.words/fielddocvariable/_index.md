---
title: 字段DocVariable
second_title: Aspose.Words for Java API Reference
description: 实现 DOCVARIABLE 字段。
type: docs
weight: 182
url: /zh/java/com.aspose.words/fielddocvariable/
---

**遗产:**
java.lang.Object, [com.aspose.words.字段](../../com.aspose.words/field)
```
public class 字段DocVariable extends 字段
```

实现 DOCVARIABLE 字段。

要了解更多信息，请访问**Working with 字段**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getDisplayResult()](#getDisplayResult--) | 获取表示显示的字段结果的文本。 |
| [getEnd()](#getEnd--) | 获取表示字段结束的节点。 |
| [get字段Code()](#get字段Code--) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [get字段Code(boolean includeChild字段Codes)](#get字段Code-boolean-) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [getFormat()](#getFormat--) | 得到一个[字段Format](../../com.aspose.words/fieldformat)提供对字段格式的类型化访问的对象。 |
| [getLocaleId()](#getLocaleId--) | 获取字段的 LCID。 |
| [getResult()](#getResult--) | 获取字段分隔符和字段结尾之间的文本。 |
| [getSeparator()](#getSeparator--) | 获取表示字段分隔符的节点。 |
| [getStart()](#getStart--) | 获取表示字段开始的节点。 |
| [get类型()](#get类型--) | 获取 Microsoft Word 字段类型。 |
| [getVariableName()](#getVariableName--) | 获取要检索的文档变量的名称。 |
| [hashCode()](#hashCode--) |  |
| [isDirty()](#isDirty--) | 获取字段的当前结果是否由于对文档进行了其他修改而不再正确（陈旧）。 |
| [isDirty(boolean value)](#isDirty-boolean-) | 设置字段的当前结果是否由于对文档的其他修改而不再正确（陈旧）。 |
| [isLocked()](#isLocked--) | 获取字段是否被锁定（不应重新计算其结果）。 |
| [isLocked(boolean value)](#isLocked-boolean-) | 设置字段是否被锁定（不应重新计算其结果）。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | 从文档中删除字段。 |
| [setLocaleId(int value)](#setLocaleId-int-) | 设置字段的 LCID。 |
| [setResult(String value)](#setResult-java.lang.String-) | 设置字段分隔符和字段结尾之间的文本。 |
| [setVariableName(String value)](#setVariableName-java.lang.String-) | 设置要检索的文档变量的名称。 |
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
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


获取字段的 LCID。

**退货:**
int - 字段的 LCID。
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
### get类型() {#get类型--}
```
public int get类型()
```


获取 Microsoft Word 字段类型。

**退货:**
 int - Microsoft Word 字段类型。返回值是以下之一[字段类型](../../com.aspose.words/fieldtype)常数。
### getVariableName() {#getVariableName--}
```
public String getVariableName()
```


获取要检索的文档变量的名称。

**退货:**
java.lang.String - 要检索的文档变量的名称。
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
### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


设置字段的 LCID。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 字段的 LCID。 |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


设置字段分隔符和字段结尾之间的文本。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 字段分隔符和字段结尾之间的文本。 |

### setVariableName(String value) {#setVariableName-java.lang.String-}
```
public void setVariableName(String value)
```


设置要检索的文档变量的名称。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 要检索的文档变量的名称。 |

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
