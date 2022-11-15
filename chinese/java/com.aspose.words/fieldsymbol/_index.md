---
title: FieldSymbol
second_title: Aspose.Words for Java API 参考
description: 实现一个符号字段。
type: docs
weight: 248
url: /zh/java/com.aspose.words/fieldsymbol/
---

**遗产:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldSymbol extends Field
```

实现一个符号字段。

要了解更多信息，请访问**Working with 字段**文档文章。

检索其代码点值以十进制或十六进制指定的字符。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getCharacterCode()](#getCharacterCode--) | 以十进制或十六进制获取字符的代码点值。 |
| [getClass()](#getClass--) |  |
| [getDisplayResult()](#getDisplayResult--) | 获取表示显示的字段结果的文本。 |
| [getDontAffectsLineSpacing()](#getDontAffectsLineSpacing--) | 获取字段检索到的字符是否影响段落的行距。 |
| [getEnd()](#getEnd--) | 获取表示字段结束的节点。 |
| [getFieldCode()](#getFieldCode--) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [getFontName()](#getFontName--) | 获取字段检索到的字符的字体名称。 |
| [getFontSize()](#getFontSize--) | 获取字段检索到的字符的字体大小（以磅为单位）。 |
| [getFormat()](#getFormat--) | 得到一个[FieldFormat](../../com.aspose.words/fieldformat)提供对字段格式的类型化访问的对象。 |
| [getLocaleId()](#getLocaleId--) | 获取字段的 LCID。 |
| [getResult()](#getResult--) | 获取字段分隔符和字段结尾之间的文本。 |
| [getSeparator()](#getSeparator--) | 获取表示字段分隔符的节点。 |
| [getStart()](#getStart--) | 获取表示字段开始的节点。 |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getType()](#getType--) | 获取 Microsoft Word 字段类型。 |
| [hashCode()](#hashCode--) |  |
| [isAnsi()](#isAnsi--) | 获取字符代码是否被解释为 ANSI 字符的值。 |
| [isAnsi(boolean value)](#isAnsi-boolean-) | 设置字符代码是否被解释为 ANSI 字符的值。 |
| [isDirty()](#isDirty--) | 获取字段的当前结果是否由于对文档进行了其他修改而不再正确（陈旧）。 |
| [isDirty(boolean value)](#isDirty-boolean-) | 设置字段的当前结果是否由于对文档的其他修改而不再正确（陈旧）。 |
| [isLocked()](#isLocked--) | 获取字段是否被锁定（不应重新计算其结果）。 |
| [isLocked(boolean value)](#isLocked-boolean-) | 设置字段是否被锁定（不应重新计算其结果）。 |
| [isShiftJis()](#isShiftJis--) | 获取字符代码是否被解释为 SHIFT-JIS 字符的值。 |
| [isShiftJis(boolean value)](#isShiftJis-boolean-) | 设置字符代码是否解释为 SHIFT-JIS 字符的值。 |
| [isUnicode()](#isUnicode--) | 获取字符代码是否被解释为 Unicode 字符的值。 |
| [isUnicode(boolean value)](#isUnicode-boolean-) | 设置字符代码是否被解释为 Unicode 字符的值。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | 从文档中删除字段。 |
| [setCharacterCode(String value)](#setCharacterCode-java.lang.String-) | 以十进制或十六进制设置字符的代码点值。 |
| [setDontAffectsLineSpacing(boolean value)](#setDontAffectsLineSpacing-boolean-) | 设置字段检索的字符是否影响段落的行距。 |
| [setFontName(String value)](#setFontName-java.lang.String-) | 设置字段检索到的字符的字体名称。 |
| [setFontSize(String value)](#setFontSize-java.lang.String-) | 设置字段检索到的字符的字体大小（以磅为单位）。 |
| [setLocaleId(int value)](#setLocaleId-int-) | 设置字段的 LCID。 |
| [setResult(String value)](#setResult-java.lang.String-) | 设置字段分隔符和字段结尾之间的文本。 |
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
### getCharacterCode() {#getCharacterCode--}
```
public String getCharacterCode()
```


以十进制或十六进制获取字符的代码点值。

**退货:**
java.lang.String - 十进制或十六进制的字符代码点值。
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
### getDontAffectsLineSpacing() {#getDontAffectsLineSpacing--}
```
public boolean getDontAffectsLineSpacing()
```


获取字段检索到的字符是否影响段落的行距。

**退货:**
boolean - 字段检索到的字符是否影响段落的行距。
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
### getFontName() {#getFontName--}
```
public String getFontName()
```


获取字段检索到的字符的字体名称。

**退货:**
java.lang.String - 字段检索到的字符的字体名称。
### getFontSize() {#getFontSize--}
```
public String getFontSize()
```


获取字段检索到的字符的字体大小（以磅为单位）。

**退货:**
java.lang.String - 字段检索到的字符的字体大小（以磅为单位）。
### getFormat() {#getFormat--}
```
public FieldFormat getFormat()
```


得到一个[FieldFormat](../../com.aspose.words/fieldformat)提供对字段格式的类型化访问的对象。

**退货:**
[FieldFormat](../../com.aspose.words/fieldformat) - 一个[FieldFormat](../../com.aspose.words/fieldformat)提供对字段格式的类型化访问的对象。
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
public FieldSeparator getSeparator()
```


获取表示字段分隔符的节点。可以为空。

**退货:**
[FieldSeparator](../../com.aspose.words/fieldseparator) - 表示字段分隔符的节点。
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
### isAnsi() {#isAnsi--}
```
public boolean isAnsi()
```


获取字符代码是否被解释为 ANSI 字符的值。

**退货:**
boolean - 字符代码是否被解释为 ANSI 字符的值。
### isAnsi(boolean value) {#isAnsi-boolean-}
```
public void isAnsi(boolean value)
```


设置字符代码是否被解释为 ANSI 字符的值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 字符代码是否被解释为 ANSI 字符的值。 |

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

### isShiftJis() {#isShiftJis--}
```
public boolean isShiftJis()
```


获取字符代码是否被解释为 SHIFT-JIS 字符的值。

**退货:**
boolean - 字符代码是否被解释为 SHIFT-JIS 字符的值。
### isShiftJis(boolean value) {#isShiftJis-boolean-}
```
public void isShiftJis(boolean value)
```


设置字符代码是否解释为 SHIFT-JIS 字符的值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 字符代码是否被解释为 SHIFT-JIS 字符的值。 |

### isUnicode() {#isUnicode--}
```
public boolean isUnicode()
```


获取字符代码是否被解释为 Unicode 字符的值。

**退货:**
boolean - 字符代码是否被解释为 Unicode 字符的值。
### isUnicode(boolean value) {#isUnicode-boolean-}
```
public void isUnicode(boolean value)
```


设置字符代码是否被解释为 Unicode 字符的值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 字符代码是否被解释为 Unicode 字符的值。 |

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
### setCharacterCode(String value) {#setCharacterCode-java.lang.String-}
```
public void setCharacterCode(String value)
```


以十进制或十六进制设置字符的代码点值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 十进制或十六进制的字符代码点值。 |

### setDontAffectsLineSpacing(boolean value) {#setDontAffectsLineSpacing-boolean-}
```
public void setDontAffectsLineSpacing(boolean value)
```


设置字段检索的字符是否影响段落的行距。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 字段检索到的字符是否影响段落的行距。 |

### setFontName(String value) {#setFontName-java.lang.String-}
```
public void setFontName(String value)
```


设置字段检索到的字符的字体名称。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 字段检索到的字符的字体名称。 |

### setFontSize(String value) {#setFontSize-java.lang.String-}
```
public void setFontSize(String value)
```


设置字段检索到的字符的字体大小（以磅为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 字段检索到的字符字体的大小（以磅为单位）。 |

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
