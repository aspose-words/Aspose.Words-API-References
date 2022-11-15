---
title: FieldToc
second_title: Aspose.Words for Java API 参考
description: 实现 TOC 字段。
type: docs
weight: 255
url: /zh/java/com.aspose.words/fieldtoc/
---

**遗产:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldToc extends Field
```

实现 TOC 字段。

要了解更多信息，请访问**Working with 字段**文档文章。

使用 TC 字段指定的条目、它们的标题级别和指定的样式构建目录（也可以是图表），并将该表插入到文档中的此位置。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAreCustomStylesSpecified()](#getAreCustomStylesSpecified--) |  |
| [getBookmarkName()](#getBookmarkName--) | 获取标记文档中用于构建表的部分的书签的名称。 |
| [getCaptionlessTableOfFiguresLabel()](#getCaptionlessTableOfFiguresLabel--) | 获取在构建不包括标题标签和数字的图形表时使用的序列标识符的名称。 |
| [getClass()](#getClass--) |  |
| [getCustomStyles()](#getCustomStyles--) | 获取要包含在目录中的除内置标题样式之外的样式列表。 |
| [getDisplayResult()](#getDisplayResult--) | 获取表示显示的字段结果的文本。 |
| [getEnd()](#getEnd--) | 获取表示字段结束的节点。 |
| [getEntryIdentifier()](#getEntryIdentifier--) | 获取一个字符串，该字符串应与包含的 TC 字段的类型标识符匹配。 |
| [getEntryLevelRange()](#getEntryLevelRange--) | 获取要包含的目录条目的一系列级别。 |
| [getEntrySeparator()](#getEntrySeparator--) | 获取分隔条目及其页码的字符序列。 |
| [getEntryTypeCore()](#getEntryTypeCore--) |  |
| [getFieldCode()](#getFieldCode--) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [getFormat()](#getFormat--) | 得到一个[FieldFormat](../../com.aspose.words/fieldformat)提供对字段格式的类型化访问的对象。 |
| [getHeadingLevelRange()](#getHeadingLevelRange--) | 获取要包含的一系列标题级别。 |
| [getHideInWebLayout()](#getHideInWebLayout--) | 获取是否在 Web 布局视图中隐藏选项卡前导和页码。 |
| [getIncludeRefDoc字段()](#getIncludeRefDoc字段--) |  |
| [getIncludeTocEntry字段()](#getIncludeTocEntry字段--) |  |
| [getInsertHyperlinks()](#getInsertHyperlinks--) | 获取是否使目录条目超链接。 |
| [getLevelForCustomStyle(Paragraph paragraph, Style style)](#getLevelForCustomStyle-com.aspose.words.Paragraph-com.aspose.words.Style-) |  |
| [getLocaleId()](#getLocaleId--) | 获取字段的 LCID。 |
| [getPageNumberOmittingLevelRange()](#getPageNumberOmittingLevelRange--) | 获取要从中省略页码的目录条目的级别范围。 |
| [getPrefixedSequenceIdentifier()](#getPrefixedSequenceIdentifier--) | 获取应将前缀添加到条目页码的序列的标识符。 |
| [getPreserveLineBreaks()](#getPreserveLineBreaks--) | 获取是否在表格条目中保留换行符。 |
| [getPreserveTabs()](#getPreserveTabs--) | 获取是否在表条目中保留选项卡条目。 |
| [getRangeBookmark()](#getRangeBookmark--) |  |
| [getResult()](#getResult--) | 获取字段分隔符和字段结尾之间的文本。 |
| [getSeparator()](#getSeparator--) | 获取表示字段分隔符的节点。 |
| [getSequenceSeparator()](#getSequenceSeparator--) | 获取用于分隔序号和页码的字符序列。 |
| [getSkipTables()](#getSkipTables--) |  |
| [getStart()](#getStart--) | 获取表示字段开始的节点。 |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getTableOfFiguresLabel()](#getTableOfFiguresLabel--) | 获取构建图形表时使用的序列标识符的名称。 |
| [getType()](#getType--) | 获取 Microsoft Word 字段类型。 |
| [getUseParagraphOutlineLevel()](#getUseParagraphOutlineLevel--) | 获取是否使用应用的段落大纲级别。 |
| [hashCode()](#hashCode--) |  |
| [isBookmarkRangeSpecified()](#isBookmarkRangeSpecified--) |  |
| [isDirty()](#isDirty--) | 获取字段的当前结果是否由于对文档进行了其他修改而不再正确（陈旧）。 |
| [isDirty(boolean value)](#isDirty-boolean-) | 设置字段的当前结果是否由于对文档的其他修改而不再正确（陈旧）。 |
| [isEntryLevelRangeSpecified()](#isEntryLevelRangeSpecified--) |  |
| [isHeadingLevelRangeSpecified()](#isHeadingLevelRangeSpecified--) |  |
| [isLocked()](#isLocked--) | 获取字段是否被锁定（不应重新计算其结果）。 |
| [isLocked(boolean value)](#isLocked-boolean-) | 设置字段是否被锁定（不应重新计算其结果）。 |
| [isTableOfFigures()](#isTableOfFigures--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | 从文档中删除字段。 |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String-) | 设置标记用于构建表的文档部分的书签的名称。 |
| [setCaptionlessTableOfFiguresLabel(String value)](#setCaptionlessTableOfFiguresLabel-java.lang.String-) | 设置在构建不包括标题标签和数字的图形表时使用的序列标识符的名称。 |
| [setCustomStyles(String value)](#setCustomStyles-java.lang.String-) | 设置包含在目录中的内置标题样式以外的样式列表。 |
| [setEntryIdentifier(String value)](#setEntryIdentifier-java.lang.String-) | 设置一个字符串，该字符串应与包含的 TC 字段的类型标识符匹配。 |
| [setEntryLevelRange(String value)](#setEntryLevelRange-java.lang.String-) | 设置要包含的目录条目的级别范围。 |
| [setEntrySeparator(String value)](#setEntrySeparator-java.lang.String-) | 设置分隔条目及其页码的字符序列。 |
| [setHeadingLevelRange(String value)](#setHeadingLevelRange-java.lang.String-) | 设置要包括的标题级别范围。 |
| [setHideInWebLayout(boolean value)](#setHideInWebLayout-boolean-) | 设置是否在 Web 布局视图中隐藏选项卡前导和页码。 |
| [setInsertHyperlinks(boolean value)](#setInsertHyperlinks-boolean-) | 设置是否使目录条目成为超链接。 |
| [setLocaleId(int value)](#setLocaleId-int-) | 设置字段的 LCID。 |
| [setPageNumberOmittingLevelRange(String value)](#setPageNumberOmittingLevelRange-java.lang.String-) | 设置目录条目的级别范围，从中省略页码。 |
| [setPrefixedSequenceIdentifier(String value)](#setPrefixedSequenceIdentifier-java.lang.String-) | 设置应为其添加前缀到条目页码的序列的标识符。 |
| [setPreserveLineBreaks(boolean value)](#setPreserveLineBreaks-boolean-) | 设置是否在表条目中保留换行符。 |
| [setPreserveTabs(boolean value)](#setPreserveTabs-boolean-) | 设置是否在表格条目中保留选项卡条目。 |
| [setResult(String value)](#setResult-java.lang.String-) | 设置字段分隔符和字段结尾之间的文本。 |
| [setSequenceSeparator(String value)](#setSequenceSeparator-java.lang.String-) | 设置用于分隔序号和页码的字符序列。 |
| [setTableOfFiguresLabel(String value)](#setTableOfFiguresLabel-java.lang.String-) | 设置构建图表时使用的序列标识符的名称。 |
| [setUseParagraphOutlineLevel(boolean value)](#setUseParagraphOutlineLevel-boolean-) | 设置是否使用应用的段落轮廓级别。 |
| [toString()](#toString--) |  |
| [unlink()](#unlink--) | 执行字段取消链接。 |
| [update()](#update--) | 执行字段更新。 |
| [update(boolean ignoreMergeFormat)](#update-boolean-) | 执行字段更新。 |
| [updatePageNumbers()](#updatePageNumbers--) | 更新此目录中项目的页码。 |
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
### getAreCustomStylesSpecified() {#getAreCustomStylesSpecified--}
```
public boolean getAreCustomStylesSpecified()
```




**退货:**
布尔值
### getBookmarkName() {#getBookmarkName--}
```
public String getBookmarkName()
```


获取标记文档中用于构建表的部分的书签的名称。

**退货:**
java.lang.String - 标记用于构建表的文档部分的书签名称。
### getCaptionlessTableOfFiguresLabel() {#getCaptionlessTableOfFiguresLabel--}
```
public String getCaptionlessTableOfFiguresLabel()
```


获取在构建不包括标题标签和数字的图形表时使用的序列标识符的名称。

**退货:**
java.lang.String - 构建不包括标题标签和编号的图表时使用的序列标识符的名称。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getCustomStyles() {#getCustomStyles--}
```
public String getCustomStyles()
```


获取要包含在目录中的除内置标题样式之外的样式列表。

**退货:**
java.lang.String - 要包含在目录中的内置标题样式以外的样式列表。
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
### getEntryIdentifier() {#getEntryIdentifier--}
```
public String getEntryIdentifier()
```


获取一个字符串，该字符串应与包含的 TC 字段的类型标识符匹配。

**退货:**
java.lang.String - 应与包含的 TC 字段的类型标识符相匹配的字符串。
### getEntryLevelRange() {#getEntryLevelRange--}
```
public String getEntryLevelRange()
```


获取要包含的目录条目的一系列级别。

**退货:**
java.lang.String - 要包含的目录条目的级别范围。
### getEntrySeparator() {#getEntrySeparator--}
```
public String getEntrySeparator()
```


获取分隔条目及其页码的字符序列。

**退货:**
java.lang.String - 分隔条目及其页码的字符序列。
### getEntryTypeCore() {#getEntryTypeCore--}
```
public int getEntryTypeCore()
```




**退货:**
整数
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
### getHeadingLevelRange() {#getHeadingLevelRange--}
```
public String getHeadingLevelRange()
```


获取要包含的一系列标题级别。

**退货:**
java.lang.String - 要包含的一系列标题级别。
### getHideInWebLayout() {#getHideInWebLayout--}
```
public boolean getHideInWebLayout()
```


获取是否在 Web 布局视图中隐藏选项卡前导和页码。

**退货:**
boolean - 是否在 Web 布局视图中隐藏制表符前导符和页码。
### getIncludeRefDoc字段() {#getIncludeRefDoc字段--}
```
public boolean getIncludeRefDoc字段()
```




**退货:**
布尔值
### getIncludeTocEntry字段() {#getIncludeTocEntry字段--}
```
public boolean getIncludeTocEntry字段()
```




**退货:**
布尔值
### getInsertHyperlinks() {#getInsertHyperlinks--}
```
public boolean getInsertHyperlinks()
```


获取是否使目录条目超链接。

**退货:**
boolean - 是否制作目录条目超链接。
### getLevelForCustomStyle(Paragraph paragraph, Style style) {#getLevelForCustomStyle-com.aspose.words.Paragraph-com.aspose.words.Style-}
```
public int getLevelForCustomStyle(Paragraph paragraph, Style style)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| paragraph | [Paragraph](../../com.aspose.words/paragraph) |  |
| style | [Style](../../com.aspose.words/style) |  |

**退货:**
整数
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


获取字段的 LCID。

**退货:**
int - 字段的 LCID。
### getPageNumberOmittingLevelRange() {#getPageNumberOmittingLevelRange--}
```
public String getPageNumberOmittingLevelRange()
```


获取要从中省略页码的目录条目的级别范围。

**退货:**
java.lang.String - 目录条目的级别范围，从中省略页码。
### getPrefixedSequenceIdentifier() {#getPrefixedSequenceIdentifier--}
```
public String getPrefixedSequenceIdentifier()
```


获取应将前缀添加到条目页码的序列的标识符。

**退货:**
java.lang.String - 应将前缀添加到条目页码的序列标识符。
### getPreserveLineBreaks() {#getPreserveLineBreaks--}
```
public boolean getPreserveLineBreaks()
```


获取是否在表格条目中保留换行符。

**退货:**
boolean - 是否在表格条目中保留换行符。
### getPreserveTabs() {#getPreserveTabs--}
```
public boolean getPreserveTabs()
```


获取是否在表条目中保留选项卡条目。

**退货:**
boolean - 是否在表格条目中保留选项卡条目。
### getRangeBookmark() {#getRangeBookmark--}
```
public Bookmark getRangeBookmark()
```




**退货:**
[Bookmark](../../com.aspose.words/bookmark)
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
### getSequenceSeparator() {#getSequenceSeparator--}
```
public String getSequenceSeparator()
```


获取用于分隔序号和页码的字符序列。

**退货:**
java.lang.String - 用于分隔序列号和页码的字符序列。
### getSkipTables() {#getSkipTables--}
```
public boolean getSkipTables()
```




**退货:**
布尔值
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
### getTableOfFiguresLabel() {#getTableOfFiguresLabel--}
```
public String getTableOfFiguresLabel()
```


获取构建图形表时使用的序列标识符的名称。

**退货:**
java.lang.String - 构建图表时使用的序列标识符的名称。
### getType() {#getType--}
```
public int getType()
```


获取 Microsoft Word 字段类型。

**退货:**
 int - Microsoft Word 字段类型。返回值是以下之一[FieldType](../../com.aspose.words/fieldtype)常数。
### getUseParagraphOutlineLevel() {#getUseParagraphOutlineLevel--}
```
public boolean getUseParagraphOutlineLevel()
```


获取是否使用应用的段落大纲级别。

**退货:**
boolean - 是否使用应用的段落轮廓级别。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isBookmarkRangeSpecified() {#isBookmarkRangeSpecified--}
```
public boolean isBookmarkRangeSpecified()
```




**退货:**
布尔值
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

### isEntryLevelRangeSpecified() {#isEntryLevelRangeSpecified--}
```
public boolean isEntryLevelRangeSpecified()
```




**退货:**
布尔值
### isHeadingLevelRangeSpecified() {#isHeadingLevelRangeSpecified--}
```
public boolean isHeadingLevelRangeSpecified()
```




**退货:**
布尔值
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

### isTableOfFigures() {#isTableOfFigures--}
```
public boolean isTableOfFigures()
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


设置标记用于构建表的文档部分的书签的名称。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 标记用于构建表格的文档部分的书签的名称。 |

### setCaptionlessTableOfFiguresLabel(String value) {#setCaptionlessTableOfFiguresLabel-java.lang.String-}
```
public void setCaptionlessTableOfFiguresLabel(String value)
```


设置在构建不包括标题标签和数字的图形表时使用的序列标识符的名称。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 构建不包括标题标签和数字的图表时使用的序列标识符的名称。 |

### setCustomStyles(String value) {#setCustomStyles-java.lang.String-}
```
public void setCustomStyles(String value)
```


设置包含在目录中的内置标题样式以外的样式列表。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 要包含在目录中的除内置标题样式之外的样式列表。 |

### setEntryIdentifier(String value) {#setEntryIdentifier-java.lang.String-}
```
public void setEntryIdentifier(String value)
```


设置一个字符串，该字符串应与包含的 TC 字段的类型标识符匹配。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 应与包含的 TC 字段的类型标识符匹配的字符串。 |

### setEntryLevelRange(String value) {#setEntryLevelRange-java.lang.String-}
```
public void setEntryLevelRange(String value)
```


设置要包含的目录条目的级别范围。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 要包含的目录条目的一系列级别。 |

### setEntrySeparator(String value) {#setEntrySeparator-java.lang.String-}
```
public void setEntrySeparator(String value)
```


设置分隔条目及其页码的字符序列。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 分隔条目及其页码的字符序列。 |

### setHeadingLevelRange(String value) {#setHeadingLevelRange-java.lang.String-}
```
public void setHeadingLevelRange(String value)
```


设置要包括的标题级别范围。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 要包括的一系列标题级别。 |

### setHideInWebLayout(boolean value) {#setHideInWebLayout-boolean-}
```
public void setHideInWebLayout(boolean value)
```


设置是否在 Web 布局视图中隐藏选项卡前导和页码。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否在 Web 布局视图中隐藏选项卡前导和页码。 |

### setInsertHyperlinks(boolean value) {#setInsertHyperlinks-boolean-}
```
public void setInsertHyperlinks(boolean value)
```


设置是否使目录条目成为超链接。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否使目录条目超链接。 |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


设置字段的 LCID。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 字段的 LCID。 |

### setPageNumberOmittingLevelRange(String value) {#setPageNumberOmittingLevelRange-java.lang.String-}
```
public void setPageNumberOmittingLevelRange(String value)
```


设置目录条目的级别范围，从中省略页码。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 要省略页码的目录条目的级别范围。 |

### setPrefixedSequenceIdentifier(String value) {#setPrefixedSequenceIdentifier-java.lang.String-}
```
public void setPrefixedSequenceIdentifier(String value)
```


设置应为其添加前缀到条目页码的序列的标识符。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 应将前缀添加到条目页码的序列标识符。 |

### setPreserveLineBreaks(boolean value) {#setPreserveLineBreaks-boolean-}
```
public void setPreserveLineBreaks(boolean value)
```


设置是否在表条目中保留换行符。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否在表格条目中保留换行符。 |

### setPreserveTabs(boolean value) {#setPreserveTabs-boolean-}
```
public void setPreserveTabs(boolean value)
```


设置是否在表格条目中保留选项卡条目。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否在表格条目中保留选项卡条目。 |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


设置字段分隔符和字段结尾之间的文本。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 字段分隔符和字段结尾之间的文本。 |

### setSequenceSeparator(String value) {#setSequenceSeparator-java.lang.String-}
```
public void setSequenceSeparator(String value)
```


设置用于分隔序号和页码的字符序列。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 用于分隔序号和页码的字符序列。 |

### setTableOfFiguresLabel(String value) {#setTableOfFiguresLabel-java.lang.String-}
```
public void setTableOfFiguresLabel(String value)
```


设置构建图表时使用的序列标识符的名称。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 构建图表时使用的序列标识符的名称。 |

### setUseParagraphOutlineLevel(boolean value) {#setUseParagraphOutlineLevel-boolean-}
```
public void setUseParagraphOutlineLevel(boolean value)
```


设置是否使用应用的段落轮廓级别。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否使用应用的段落轮廓级别。 |

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

### updatePageNumbers() {#updatePageNumbers--}
```
public boolean updatePageNumbers()
```


更新此目录中项目的页码。

**退货:**
boolean - 如果操作成功则为真。如果删除了任何相关的 TOC 书签，将返回 false。
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
