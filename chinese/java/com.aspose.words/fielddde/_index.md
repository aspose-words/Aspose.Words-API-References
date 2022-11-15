---
title: FieldDde
second_title: Aspose.Words for Java API 参考
description: 实现 DDE 字段。
type: docs
weight: 178
url: /zh/java/com.aspose.words/fielddde/
---

**遗产:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldDde extends Field
```

实现 DDE 字段。

要了解更多信息，请访问**Working with 字段**文档文章。

对于从另一个应用程序复制的信息，此字段使用 DDE 将该信息链接到其原始源文件。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAutoUpdate()](#getAutoUpdate--) | 获取是否自动更新该字段。 |
| [getClass()](#getClass--) |  |
| [getDisplayResult()](#getDisplayResult--) | 获取表示显示的字段结果的文本。 |
| [getEnd()](#getEnd--) | 获取表示字段结束的节点。 |
| [getFieldCode()](#getFieldCode--) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [getFormat()](#getFormat--) | 得到一个[FieldFormat](../../com.aspose.words/fieldformat)提供对字段格式的类型化访问的对象。 |
| [getInsertAsBitmap()](#getInsertAsBitmap--) | 获取是否将链接对象作为位图插入。 |
| [getInsertAsHtml()](#getInsertAsHtml--) | 获取是否将链接对象作为 HTML 格式文本插入。 |
| [getInsertAsPicture()](#getInsertAsPicture--) | 获取是否将链接对象作为图片插入。 |
| [getInsertAsRtf()](#getInsertAsRtf--) | 获取是否以富文本格式 (RTF) 插入链接对象。 |
| [getInsertAsText()](#getInsertAsText--) | 获取是否以纯文本格式插入链接对象。 |
| [getInsertAsUnicode()](#getInsertAsUnicode--) | 获取是否将链接对象作为 Unicode 文本插入。 |
| [getLocaleId()](#getLocaleId--) | 获取字段的 LCID。 |
| [getProgId()](#getProgId--) | 获取链接信息的应用类型。 |
| [getResult()](#getResult--) | 获取字段分隔符和字段结尾之间的文本。 |
| [getSeparator()](#getSeparator--) | 获取表示字段分隔符的节点。 |
| [getSourceFullName()](#getSourceFullName--) | 获取源文件的名称和位置。 |
| [getSourceItem()](#getSourceItem--) | 获取正在链接的源文件部分。 |
| [getStart()](#getStart--) | 获取表示字段开始的节点。 |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getType()](#getType--) | 获取 Microsoft Word 字段类型。 |
| [hashCode()](#hashCode--) |  |
| [isDirty()](#isDirty--) | 获取字段的当前结果是否由于对文档进行了其他修改而不再正确（陈旧）。 |
| [isDirty(boolean value)](#isDirty-boolean-) | 设置字段的当前结果是否由于对文档的其他修改而不再正确（陈旧）。 |
| [isLinked()](#isLinked--) | 获取是否通过不将图形数据与文档一起存储来减小文件大小。 |
| [isLinked(boolean value)](#isLinked-boolean-) | 设置是否通过不将图形数据与文档一起存储来减小文件大小。 |
| [isLocked()](#isLocked--) | 获取字段是否被锁定（不应重新计算其结果）。 |
| [isLocked(boolean value)](#isLocked-boolean-) | 设置字段是否被锁定（不应重新计算其结果）。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | 从文档中删除字段。 |
| [setAutoUpdate(boolean value)](#setAutoUpdate-boolean-) | 设置是否自动更新该字段。 |
| [setInsertAsBitmap(boolean value)](#setInsertAsBitmap-boolean-) | 设置是否将链接对象作为位图插入。 |
| [setInsertAsHtml(boolean value)](#setInsertAsHtml-boolean-) | 设置是否将链接对象作为 HTML 格式文本插入。 |
| [setInsertAsPicture(boolean value)](#setInsertAsPicture-boolean-) | 设置是否将链接对象作为图片插入。 |
| [setInsertAsRtf(boolean value)](#setInsertAsRtf-boolean-) | 设置是否以富文本格式 (RTF) 插入链接对象。 |
| [setInsertAsText(boolean value)](#setInsertAsText-boolean-) | 设置是否以纯文本格式插入链接对象。 |
| [setInsertAsUnicode(boolean value)](#setInsertAsUnicode-boolean-) | 设置是否将链接对象作为 Unicode 文本插入。 |
| [setLocaleId(int value)](#setLocaleId-int-) | 设置字段的 LCID。 |
| [setProgId(String value)](#setProgId-java.lang.String-) | 设置链接信息的应用类型。 |
| [setResult(String value)](#setResult-java.lang.String-) | 设置字段分隔符和字段结尾之间的文本。 |
| [setSourceFullName(String value)](#setSourceFullName-java.lang.String-) | 设置源文件的名称和位置。 |
| [setSourceItem(String value)](#setSourceItem-java.lang.String-) | 设置被链接的源文件部分。 |
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
### getAutoUpdate() {#getAutoUpdate--}
```
public boolean getAutoUpdate()
```


获取是否自动更新该字段。

**退货:**
boolean - 是否自动更新这个字段。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
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
### getInsertAsBitmap() {#getInsertAsBitmap--}
```
public boolean getInsertAsBitmap()
```


获取是否将链接对象作为位图插入。

**退货:**
boolean - 是否将链接对象作为位图插入。
### getInsertAsHtml() {#getInsertAsHtml--}
```
public boolean getInsertAsHtml()
```


获取是否将链接对象作为 HTML 格式文本插入。

**退货:**
boolean - 是否将链接对象作为 HTML 格式文本插入。
### getInsertAsPicture() {#getInsertAsPicture--}
```
public boolean getInsertAsPicture()
```


获取是否将链接对象作为图片插入。

**退货:**
boolean - 是否将链接对象作为图片插入。
### getInsertAsRtf() {#getInsertAsRtf--}
```
public boolean getInsertAsRtf()
```


获取是否以富文本格式 (RTF) 插入链接对象。

**退货:**
boolean - 是否以富文本格式 (RTF) 插入链接对象。
### getInsertAsText() {#getInsertAsText--}
```
public boolean getInsertAsText()
```


获取是否以纯文本格式插入链接对象。

**退货:**
boolean - 是否以纯文本格式插入链接对象。
### getInsertAsUnicode() {#getInsertAsUnicode--}
```
public boolean getInsertAsUnicode()
```


获取是否将链接对象作为 Unicode 文本插入。

**退货:**
boolean - 是否将链接对象作为 Unicode 文本插入。
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


获取字段的 LCID。

**退货:**
int - 字段的 LCID。
### getProgId() {#getProgId--}
```
public String getProgId()
```


获取链接信息的应用类型。

**退货:**
java.lang.String - 链接信息的应用类型。
### getResult() {#getResult--}
```
public String getResult()
```


获取字段分隔符和字段结尾之间的文本。

**退货:**
java.lang.String - 字段分隔符和字段结尾之间的文本。
### getSeparator() {#getSeparator--}
```
public FieldSeparator getSeparator()
```


获取表示字段分隔符的节点。可以为空。

**退货:**
[FieldSeparator](../../com.aspose.words/fieldseparator) - 表示字段分隔符的节点。
### getSourceFullName() {#getSourceFullName--}
```
public String getSourceFullName()
```


获取源文件的名称和位置。

**退货:**
java.lang.String - 源文件的名称和位置。
### getSourceItem() {#getSourceItem--}
```
public String getSourceItem()
```


获取正在链接的源文件部分。

**退货:**
java.lang.String - 被链接的源文件部分。
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

### isLinked() {#isLinked--}
```
public boolean isLinked()
```


获取是否通过不将图形数据与文档一起存储来减小文件大小。

**退货:**
boolean - 是否通过不将图形数据与文档一起存储来减小文件大小。
### isLinked(boolean value) {#isLinked-boolean-}
```
public void isLinked(boolean value)
```


设置是否通过不将图形数据与文档一起存储来减小文件大小。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否通过不将图形数据与文档一起存储来减小文件大小。 |

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
### setAutoUpdate(boolean value) {#setAutoUpdate-boolean-}
```
public void setAutoUpdate(boolean value)
```


设置是否自动更新该字段。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否自动更新该字段。 |

### setInsertAsBitmap(boolean value) {#setInsertAsBitmap-boolean-}
```
public void setInsertAsBitmap(boolean value)
```


设置是否将链接对象作为位图插入。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否将链接对象作为位图插入。 |

### setInsertAsHtml(boolean value) {#setInsertAsHtml-boolean-}
```
public void setInsertAsHtml(boolean value)
```


设置是否将链接对象作为 HTML 格式文本插入。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否将链接对象作为 HTML 格式文本插入。 |

### setInsertAsPicture(boolean value) {#setInsertAsPicture-boolean-}
```
public void setInsertAsPicture(boolean value)
```


设置是否将链接对象作为图片插入。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否将链接对象作为图片插入。 |

### setInsertAsRtf(boolean value) {#setInsertAsRtf-boolean-}
```
public void setInsertAsRtf(boolean value)
```


设置是否以富文本格式 (RTF) 插入链接对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否以富文本格式 (RTF) 插入链接对象。 |

### setInsertAsText(boolean value) {#setInsertAsText-boolean-}
```
public void setInsertAsText(boolean value)
```


设置是否以纯文本格式插入链接对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否以纯文本格式插入链接对象。 |

### setInsertAsUnicode(boolean value) {#setInsertAsUnicode-boolean-}
```
public void setInsertAsUnicode(boolean value)
```


设置是否将链接对象作为 Unicode 文本插入。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否将链接对象作为 Unicode 文本插入。 |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


设置字段的 LCID。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 字段的 LCID。 |

### setProgId(String value) {#setProgId-java.lang.String-}
```
public void setProgId(String value)
```


设置链接信息的应用类型。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 链接信息的应用类型。 |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


设置字段分隔符和字段结尾之间的文本。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 字段分隔符和字段结尾之间的文本。 |

### setSourceFullName(String value) {#setSourceFullName-java.lang.String-}
```
public void setSourceFullName(String value)
```


设置源文件的名称和位置。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 源文件的名称和位置。 |

### setSourceItem(String value) {#setSourceItem-java.lang.String-}
```
public void setSourceItem(String value)
```


设置被链接的源文件部分。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 被链接的源文件部分。 |

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
