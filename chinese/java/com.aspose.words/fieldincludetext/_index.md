---
title: 字段IncludeText
second_title: Aspose.Words for Java API 参考
description:实现 INCLUDETEXT 字段。
type: docs
weight: 205
url: /zh/java/com.aspose.words/fieldincludetext/
---

**遗产:**
java.lang.Object, [com.aspose.words.字段](../../com.aspose.words/field)
```
public class 字段IncludeText extends 字段
```

实现 INCLUDETEXT 字段。

要了解更多信息，请访问**Working with 字段**文档文章。

插入包含在另一个文档中的全部或部分文本和图形。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBookmarkName()](#getBookmarkName--) | 获取文档中要包含的书签的名称。 |
| [get班级()](#get班级--) |  |
| [getDisplayResult()](#getDisplayResult--) | 获取表示显示的字段结果的文本。 |
| [getEncoding()](#getEncoding--) | 获取应用于引用文件中数据的编码。 |
| [getEnd()](#getEnd--) | 获取表示字段结束的节点。 |
| [get字段Code()](#get字段Code--) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [get字段Code(boolean includeChild字段Codes)](#get字段Code-boolean-) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [getFormat()](#getFormat--) | 得到一个[字段Format](../../com.aspose.words/fieldformat)提供对字段格式的类型化访问的对象。 |
| [getLocaleId()](#getLocaleId--) | 获取字段的 LCID。 |
| [getLock字段()](#getLock字段--) | 获取是否阻止更新包含文档中的字段。 |
| [getMime类型()](#getMime类型--) | 获取引用文件的 MIME 类型。 |
| [getNamespaceMappings()](#getNamespaceMappings--) | 获取 XPath 查询的命名空间映射。 |
| [getResult()](#getResult--) | 获取字段分隔符和字段结尾之间的文本。 |
| [getSeparator()](#getSeparator--) | 获取表示字段分隔符的节点。 |
| [getSourceFullName()](#getSourceFullName--) | 使用 IRI 获取文档的位置。 |
| [getSourceFullNameArgumentIndex()](#getSourceFullNameArgumentIndex--) |  |
| [getStart()](#getStart--) | 获取表示字段开始的节点。 |
| [getSwitch类型(String switchName)](#getSwitch类型-java.lang.String-) |  |
| [getTextConverter()](#getTextConverter--) | 获取包含文件格式的文本转换器的名称。 |
| [get类型()](#get类型--) | 获取 Microsoft Word 字段类型。 |
| [getXPath()](#getXPath--) | 获取 XML 文件所需部分的 XPath。 |
| [getXslTransformation()](#getXslTransformation--) | 获取 XSL 转换的位置以格式化 XML 数据。 |
| [hashCode()](#hashCode--) |  |
| [isDirty()](#isDirty--) | 获取字段的当前结果是否由于对文档进行了其他修改而不再正确（陈旧）。 |
| [isDirty(boolean value)](#isDirty-boolean-) | 设置字段的当前结果是否由于对文档的其他修改而不再正确（陈旧）。 |
| [isLocked()](#isLocked--) | 获取字段是否被锁定（不应重新计算其结果）。 |
| [isLocked(boolean value)](#isLocked-boolean-) | 设置字段是否被锁定（不应重新计算其结果）。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | 从文档中删除字段。 |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String-) | 设置要包含的文档中书签的名称。 |
| [setEncoding(String value)](#setEncoding-java.lang.String-) | 设置应用于引用文件中数据的编码。 |
| [setLocaleId(int value)](#setLocaleId-int-) | 设置字段的 LCID。 |
| [setLock字段(boolean value)](#setLock字段-boolean-) | 设置是否阻止更新包含文档中的字段。 |
| [setMime类型(String value)](#setMime类型-java.lang.String-) | 设置引用文件的 MIME 类型。 |
| [setNamespaceMappings(String value)](#setNamespaceMappings-java.lang.String-) | 为 XPath 查询设置命名空间映射。 |
| [setResult(String value)](#setResult-java.lang.String-) | 设置字段分隔符和字段结尾之间的文本。 |
| [setSourceFullName(String value)](#setSourceFullName-java.lang.String-) | 使用 IRI 设置文档的位置。 |
| [setTextConverter(String value)](#setTextConverter-java.lang.String-) | 为包含文件的格式设置文本转换器的名称。 |
| [setXPath(String value)](#setXPath-java.lang.String-) | 为 XML 文件的所需部分设置 XPath。 |
| [setXslTransformation(String value)](#setXslTransformation-java.lang.String-) | 设置 XSL 转换的位置以格式化 XML 数据。 |
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


获取文档中要包含的书签的名称。

**退货:**
java.lang.String - 文档中要包含的书签的名称。
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
### getEncoding() {#getEncoding--}
```
public String getEncoding()
```


获取应用于引用文件中数据的编码。

**退货:**
java.lang.String - 应用于引用文件中数据的编码。
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
### getLock字段() {#getLock字段--}
```
public boolean getLock字段()
```


获取是否阻止更新包含文档中的字段。

**退货:**
boolean - 是否阻止包含文档中的字段被更新。
### getMime类型() {#getMime类型--}
```
public String getMime类型()
```


获取引用文件的 MIME 类型。

**退货:**
java.lang.String - 引用文件的 MIME 类型。
### getNamespaceMappings() {#getNamespaceMappings--}
```
public String getNamespaceMappings()
```


获取 XPath 查询的命名空间映射。

**退货:**
java.lang.String - XPath 查询的命名空间映射。
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
### getSourceFullName() {#getSourceFullName--}
```
public String getSourceFullName()
```


使用 IRI 获取文档的位置。

**退货:**
java.lang.String - 使用 IRI 的文档的位置。
### getSourceFullNameArgumentIndex() {#getSourceFullNameArgumentIndex--}
```
public int getSourceFullNameArgumentIndex()
```




**退货:**
整数
### getStart() {#getStart--}
```
public 字段Start getStart()
```


获取表示字段开始的节点。

**退货:**
[字段Start](../../com.aspose.words/fieldstart) - 表示字段开始的节点。
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
### getTextConverter() {#getTextConverter--}
```
public String getTextConverter()
```


获取包含文件格式的文本转换器的名称。

**退货:**
java.lang.String - 包含文件格式的文本转换器的名称。
### get类型() {#get类型--}
```
public int get类型()
```


获取 Microsoft Word 字段类型。

**退货:**
 int - Microsoft Word 字段类型。返回值是以下之一[字段类型](../../com.aspose.words/fieldtype)常数。
### getXPath() {#getXPath--}
```
public String getXPath()
```


获取 XML 文件所需部分的 XPath。

**退货:**
java.lang.String - XML 文件所需部分的 XPath。
### getXslTransformation() {#getXslTransformation--}
```
public String getXslTransformation()
```


获取 XSL 转换的位置以格式化 XML 数据。

**退货:**
java.lang.String - 用于格式化 XML 数据的 XSL 转换的位置。
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


设置要包含的文档中书签的名称。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 要包含的文档中书签的名称。 |

### setEncoding(String value) {#setEncoding-java.lang.String-}
```
public void setEncoding(String value)
```


设置应用于引用文件中数据的编码。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 应用于引用文件中数据的编码。 |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


设置字段的 LCID。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 字段的 LCID。 |

### setLock字段(boolean value) {#setLock字段-boolean-}
```
public void setLock字段(boolean value)
```


设置是否阻止更新包含文档中的字段。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否阻止更新包含文档中的字段。 |

### setMime类型(String value) {#setMime类型-java.lang.String-}
```
public void setMime类型(String value)
```


设置引用文件的 MIME 类型。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 引用文件的 MIME 类型。 |

### setNamespaceMappings(String value) {#setNamespaceMappings-java.lang.String-}
```
public void setNamespaceMappings(String value)
```


为 XPath 查询设置命名空间映射。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | XPath 查询的名称空间映射。 |

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


使用 IRI 设置文档的位置。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 使用 IRI 的文档位置。 |

### setTextConverter(String value) {#setTextConverter-java.lang.String-}
```
public void setTextConverter(String value)
```


为包含文件的格式设置文本转换器的名称。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 包含文件格式的文本转换器的名称。 |

### setXPath(String value) {#setXPath-java.lang.String-}
```
public void setXPath(String value)
```


为 XML 文件的所需部分设置 XPath。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | XML 文件所需部分的 XPath。 |

### setXslTransformation(String value) {#setXslTransformation-java.lang.String-}
```
public void setXslTransformation(String value)
```


设置 XSL 转换的位置以格式化 XML 数据。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 用于格式化 XML 数据的 XSL 转换的位置。 |

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