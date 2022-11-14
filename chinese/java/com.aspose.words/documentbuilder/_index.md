---
title: DocumentBuilder
second_title: Aspose.Words for Java API 参考
description: 提供插入文本图像和其他内容的方法，指定字体段落和节格式。
type: docs
weight: 122
url: /zh/java/com.aspose.words/documentbuilder/
---

**遗产:**
java.lang.Object
```
public class DocumentBuilder
```

提供插入文本、图像和其他内容、指定字体、段落和部分格式的方法。

要了解更多信息，请访问**Document Builder Overview**文档文章。

**DocumentBuilder**使构建过程**Document**更轻松。**Document**是由节点树组成的复合对象，虽然可以将内容节点直接插入树中，但需要对树结构有很好的理解。**DocumentBuilder**是复杂结构的“门面”**Document**并允许快速轻松地插入内容和格式。

创建一个**DocumentBuilder**并将其与[getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-).

这**DocumentBuilder**有一个内部光标，当您调用时将在其中插入文本[write(java.lang.String)](../../com.aspose.words/documentbuilder\#write-java.lang.String-), [writeln(java.lang.String)](../../com.aspose.words/documentbuilder\#writeln-java.lang.String-), **M:Aspose.Words.DocumentBuilder.InsertBreak(Aspose.Words.BreakType)**和其他方法。您可以浏览**DocumentBuilder**使用各种 MoveToXXX 方法将光标移动到文档中的不同位置。

使用[getFont()](../../com.aspose.words/documentbuilder\#getFont--)属性来指定将应用于从文档中当前位置开始插入的所有文本的字符格式。

使用[getParagraphFormat()](../../com.aspose.words/documentbuilder\#getParagraphFormat--)属性来指定将插入的当前和所有段落的段落格式。

使用[getPageSetup()](../../com.aspose.words/documentbuilder\#getPageSetup--)属性来指定当前部分和将插入的所有部分的页面和部分属性。

使用[getCellFormat()](../../com.aspose.words/documentbuilder\#getCellFormat--)和[getRowFormat()](../../com.aspose.words/documentbuilder\#getRowFormat--)属性来指定表格单元格和行的格式属性。用户[insertCell()](../../com.aspose.words/documentbuilder\#insertCell--)和[endRow()](../../com.aspose.words/documentbuilder\#endRow--)建表的方法。

注意**Font**, **ParagraphFormat**和**PageSetup**每当您导航到文档中的不同位置时，属性都会更新，以反映新位置可用的格式属性。
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [DocumentBuilder()](#DocumentBuilder--) | 初始化此类的新实例。 |
| [DocumentBuilder(Document doc)](#DocumentBuilder-com.aspose.words.Document-) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [clearCellAttrs()](#clearCellAttrs--) |  |
| [clearRowAttrs()](#clearRowAttrs--) |  |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [deleteRow(int tableIndex, int rowIndex)](#deleteRow-int-int-) | 从表中删除一行。 |
| [endBookmark(String bookmarkName)](#endBookmark-java.lang.String-) | 将文档中的当前位置标记为书签结束。 |
| [endColumnBookmark(String bookmarkName)](#endColumnBookmark-java.lang.String-) | 将文档中的当前位置标记为列书签结束。 |
| [endEditableRange()](#endEditableRange--) | 将文档中的当前位置标记为可编辑范围结束。 |
| [endEditableRange(EditableRangeStart start)](#endEditableRange-com.aspose.words.EditableRangeStart-) | 将文档中的当前位置标记为可编辑范围结束。 |
| [endRow()](#endRow--) | 结束文档中的表格行。 |
| [endTable()](#endTable--) | 结束文档中的表格。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchCellAttr(int key)](#fetchCellAttr-int-) |  |
| [fetchInheritedCellAttr(int key)](#fetchInheritedCellAttr-int-) |  |
| [fetchInheritedRowAttr(int key)](#fetchInheritedRowAttr-int-) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int-) |  |
| [fetchRowAttr(int key)](#fetchRowAttr-int-) |  |
| [getBold()](#getBold--) | 如果字体格式为粗体，则为真。 |
| [getCellFormat()](#getCellFormat--) | 返回表示当前表格单元格格式化属性的对象。 |
| [getClass()](#getClass--) |  |
| [getCurrentNode()](#getCurrentNode--) | 获取当前在此 DocumentBuilder 中选择的节点。 |
| [getCurrentParagraph()](#getCurrentParagraph--) | 获取当前在此 DocumentBuilder 中选择的段落。 |
| [getCurrentSection()](#getCurrentSection--) | 获取当前在此 DocumentBuilder 中选择的部分。 |
| [getCurrentStory()](#getCurrentStory--) | 获取当前在此 DocumentBuilder 中选择的故事。 |
| [getCurrentStructuredDocumentTag()](#getCurrentStructuredDocumentTag--) | 获取当前在此 DocumentBuilder 中选择的结构化文档标记。 |
| [getDirectCellAttr(int key)](#getDirectCellAttr-int-) |  |
| [getDirectRowAttr(int key)](#getDirectRowAttr-int-) |  |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int-) |  |
| [getDocument()](#getDocument--) | 获取[getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-)该对象附加到的对象。 |
| [getFont()](#getFont--) | 返回表示当前字体格式属性的对象。 |
| [getItalic()](#getItalic--) | 如果字体格式为斜体，则为真。 |
| [getListFormat()](#getListFormat--) | 返回表示当前列表格式属性的对象。 |
| [getPageSetup()](#getPageSetup--) | 返回表示当前页面设置和部分属性的对象。 |
| [getParagraphFormat()](#getParagraphFormat--) | 返回表示当前段落格式属性的对象。 |
| [getRowFormat()](#getRowFormat--) | 返回表示当前表行格式设置属性的对象。 |
| [getUnderline()](#getUnderline--) | 获取/设置当前字体的下划线类型。 |
| [hashCode()](#hashCode--) |  |
| [insertBreak(int breakType)](#insertBreak-int-) |  |
| [insertCell()](#insertCell--) | 在文档中插入表格单元格。 |
| [insertChart(int chartType, double width, double height)](#insertChart-int-double-double-) |  |
| [insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertChart-int-int-double-int-double-double-double-int-) |  |
| [insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size)](#insertCheckBox-java.lang.String-boolean-boolean-int-) | 在当前位置插入一个复选框表单域。 |
| [insertCheckBox(String name, boolean checkedValue, int size)](#insertCheckBox-java.lang.String-boolean-int-) | 在当前位置插入一个复选框表单域。 |
| [insertComboBox(String name, String[] items, int selectedIndex)](#insertComboBox-java.lang.String-java.lang.String---int-) | 在当前位置插入一个组合框表单域。 |
| [insertDocument(Document srcDoc, int importFormatMode)](#insertDocument-com.aspose.words.Document-int-) |  |
| [insertDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#insertDocument-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions-) |  |
| [insertField(int fieldType, boolean updateField)](#insertField-int-boolean-) |  |
| [insertField(String fieldCode)](#insertField-java.lang.String-) | 将 Word 域插入到文档中。 |
| [insertField(String fieldCode, String fieldValue)](#insertField-java.lang.String-java.lang.String-) | 将 Word 字段插入文档而不更新字段结果。 |
| [insertFootnote(int footnoteType, String footnoteText)](#insertFootnote-int-java.lang.String-) |  |
| [insertFootnote(int footnoteType, String footnoteText, String referenceMark)](#insertFootnote-int-java.lang.String-java.lang.String-) |  |
| [insertHorizontalRule()](#insertHorizontalRule--) | 在文档中插入水平线形状。 |
| [insertHtml(String html)](#insertHtml-java.lang.String-) | 将 HTML 字符串插入到文档中。 |
| [insertHtml(String html, boolean useBuilderFormatting)](#insertHtml-java.lang.String-boolean-) | 将 HTML 字符串插入到文档中。 |
| [insertHtml(String html, int options)](#insertHtml-java.lang.String-int-) |  |
| [insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark)](#insertHyperlink-java.lang.String-java.lang.String-boolean-) | 在文档中插入超链接。 |
| [insertImage(byte[] imageBytes)](#insertImage-byte---) | 将字节数组中的图像插入到文档中。 |
| [insertImage(byte[] imageBytes, double width, double height)](#insertImage-byte---double-double-) | 将字节数组中的内联图像插入文档并将其缩放到指定大小。 |
| [insertImage(byte[] imageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-byte---int-double-int-double-double-double-int-) |  |
| [insertImage(BufferedImage image)](#insertImage-java.awt.image.BufferedImage-) | 在文档中插入图像。 |
| [insertImage(BufferedImage image, double width, double height)](#insertImage-java.awt.image.BufferedImage-double-double-) | 将来自对象的内嵌图像插入到文档中并将其缩放到指定的大小。 |
| [insertImage(BufferedImage image, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.awt.image.BufferedImage-int-double-int-double-double-double-int-) |  |
| [insertImage(InputStream stream)](#insertImage-java.io.InputStream-) |  |
| [insertImage(InputStream stream, double width, double height)](#insertImage-java.io.InputStream-double-double-) |  |
| [insertImage(InputStream stream, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.io.InputStream-int-double-int-double-double-double-int-) |  |
| [insertImage(String fileName)](#insertImage-java.lang.String-) | 将文件或 URL 中的图像插入到文档中。 |
| [insertImage(String fileName, double width, double height)](#insertImage-java.lang.String-double-double-) | 将文件或 URL 中的内联图像插入到文档中，并将其缩放到指定的大小。 |
| [insertImage(String fileName, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.lang.String-int-double-int-double-double-double-int-) |  |
| [insertNode(Node node)](#insertNode-com.aspose.words.Node-) | 在光标前插入一个节点。 |
| [insertOleObject(InputStream stream, String progId, boolean asIcon, InputStream presentation)](#insertOleObject-java.io.InputStream-java.lang.String-boolean-java.io.InputStream-) |  |
| [insertOleObject(String fileName, boolean isLinked, boolean asIcon, InputStream presentation)](#insertOleObject-java.lang.String-boolean-boolean-java.io.InputStream-) |  |
| [insertOleObject(String fileName, String progId, boolean isLinked, boolean asIcon, InputStream presentation)](#insertOleObject-java.lang.String-java.lang.String-boolean-boolean-java.io.InputStream-) |  |
| [insertOleObjectAsIcon(InputStream stream, String progId, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.io.InputStream-java.lang.String-java.lang.String-java.lang.String-) |  |
| [insertOleObjectAsIcon(String fileName, boolean isLinked, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.lang.String-boolean-java.lang.String-java.lang.String-) | 将嵌入或链接的 OLE 对象作为图标插入到文档中。 |
| [insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.lang.String-java.lang.String-boolean-java.lang.String-java.lang.String-) | 将嵌入或链接的 OLE 对象作为图标插入到文档中。 |
| [insertOnlineVideo(String videoUrl, double width, double height)](#insertOnlineVideo-java.lang.String-double-double-) | 将在线视频对象插入文档并将其缩放到指定大小。 |
| [insertOnlineVideo(String videoUrl, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertOnlineVideo-java.lang.String-int-double-int-double-double-double-int-) |  |
| [insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height)](#insertOnlineVideo-java.lang.String-java.lang.String-byte---double-double-) | 将在线视频对象插入文档并将其缩放到指定大小。 |
| [insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertOnlineVideo-java.lang.String-java.lang.String-byte---int-double-int-double-double-double-int-) |  |
| [insertParagraph()](#insertParagraph--) | 在文档中插入段落分隔符。 |
| [insertShape(int shapeType, double width, double height)](#insertShape-int-double-double-) |  |
| [insertShape(int shapeType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertShape-int-int-double-int-double-double-double-int-) |  |
| [insertSignatureLine(SignatureLineOptions signatureLineOptions)](#insertSignatureLine-com.aspose.words.SignatureLineOptions-) | 在当前位置插入签名行。 |
| [insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType)](#insertSignatureLine-com.aspose.words.SignatureLineOptions-int-double-int-double-int-) |  |
| [insertStyleSeparator()](#insertStyleSeparator--) | 在文档中插入样式分隔符。 |
| [insertTableOfContents(String switches)](#insertTableOfContents-java.lang.String-) | 在文档中插入一个 TOC（目录）字段。 |
| [insertTextInput(String name, int type, String format, String fieldValue, int maxLength)](#insertTextInput-java.lang.String-int-java.lang.String-java.lang.String-int-) |  |
| [isAtEndOfParagraph()](#isAtEndOfParagraph--) | 如果光标位于当前段落的末尾，则返回 true。 |
| [isAtEndOfStructuredDocumentTag()](#isAtEndOfStructuredDocumentTag--) | 退货**true**如果光标位于结构化文档标签的末尾。 |
| [isAtStartOfParagraph()](#isAtStartOfParagraph--) | 如果光标位于当前段落的开头（光标前没有文本），则返回 true。 |
| [moveTo(Node node)](#moveTo-com.aspose.words.Node-) | 将光标移动到内联节点或段落末尾。 |
| [moveToBookmark(String bookmarkName)](#moveToBookmark-java.lang.String-) | 将光标移动到书签。 |
| [moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter)](#moveToBookmark-java.lang.String-boolean-boolean-) | 以更高的精度将光标移动到书签。 |
| [moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)](#moveToCell-int-int-int-int-) | 将光标移动到当前部分中的表格单元格。 |
| [moveToDocumentEnd()](#moveToDocumentEnd--) | 将光标移动到文档的末尾。 |
| [moveToDocumentStart()](#moveToDocumentStart--) | 将光标移动到文档的开头。 |
| [moveToField(Field field, boolean isAfter)](#moveToField-com.aspose.words.Field-boolean-) | 将光标移动到文档中的某个字段。 |
| [moveToHeaderFooter(int headerFooterType)](#moveToHeaderFooter-int-) |  |
| [moveToMergeField(String fieldName)](#moveToMergeField-java.lang.String-) | 将光标移动到指定的合并字段。 |
| [moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField)](#moveToMergeField-java.lang.String-boolean-boolean-) | 将合并字段移动到指定的合并字段。 |
| [moveToParagraph(int paragraphIndex, int characterIndex)](#moveToParagraph-int-int-) | 将光标移动到当前节中的段落。 |
| [moveToSection(int sectionIndex)](#moveToSection-int-) | 将光标移动到指定部分的正文开头。 |
| [moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex)](#moveToStructuredDocumentTag-com.aspose.words.StructuredDocumentTag-int-) | 将光标移动到结构化文档标签。 |
| [moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)](#moveToStructuredDocumentTag-int-int-) | 将光标移动到当前部分中的结构化文档标签。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [popFont()](#popFont--) | 检索以前保存在堆栈中的字符格式。 |
| [pushFont()](#pushFont--) | 将当前字符格式保存到堆栈中。 |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [resetToDefaultAttrs()](#resetToDefaultAttrs--) |  |
| [setBold(boolean value)](#setBold-boolean-) | 如果字体格式为粗体，则为真。 |
| [setCellAttr(int key, Object value)](#setCellAttr-int-java.lang.Object-) |  |
| [setDocument(Document value)](#setDocument-com.aspose.words.Document-) | 设置[getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-)该对象附加到的对象。 |
| [setItalic(boolean value)](#setItalic-boolean-) | 如果字体格式为斜体，则为真。 |
| [setRowAttr(int key, Object value)](#setRowAttr-int-java.lang.Object-) |  |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [setUnderline(int value)](#setUnderline-int-) | 获取/设置当前字体的下划线类型。 |
| [startBookmark(String bookmarkName)](#startBookmark-java.lang.String-) | 将文档中的当前位置标记为书签开始。 |
| [startColumnBookmark(String bookmarkName)](#startColumnBookmark-java.lang.String-) | 将文档中的当前位置标记为列书签开始。 |
| [startEditableRange()](#startEditableRange--) | 将文档中的当前位置标记为可编辑范围的起点。 |
| [startTable()](#startTable--) | 在文档中开始一个表格。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
| [write(String text)](#write-java.lang.String-) | 在文档的当前插入位置插入一个字符串。 |
| [writeln()](#writeln--) | 在文档中插入段落分隔符。 |
| [writeln(String text)](#writeln-java.lang.String-) | 在文档中插入一个字符串和一个段落分隔符。 |
### DocumentBuilder() {#DocumentBuilder--}
```
public DocumentBuilder()
```


初始化此类的新实例。创建一个新的**DocumentBuilder**对象并将其附加到一个新的[getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-)目的。

### DocumentBuilder(Document doc) {#DocumentBuilder-com.aspose.words.Document-}
```
public DocumentBuilder(Document doc)
```


初始化此类的新实例。创建一个新的**DocumentBuilder**对象，附加到指定[getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-)目的。光标位于文档的开头。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document) | 要附加到的文档对象。 |

### clearCellAttrs() {#clearCellAttrs--}
```
public void clearCellAttrs()
```




### clearRowAttrs() {#clearRowAttrs--}
```
public void clearRowAttrs()
```




### clearRunAttrs() {#clearRunAttrs--}
```
public void clearRunAttrs()
```




### deleteRow(int tableIndex, int rowIndex) {#deleteRow-int-int-}
```
public Row deleteRow(int tableIndex, int rowIndex)
```


从表中删除一行。

如果光标位于要删除的行内，则光标移出到下一行或表格后的下一段。

如果从只包含一行的表中删除一行，则整个表将被删除。

对于index参数，当index大于等于0时，指定从头开始的一个索引，0为第一个元素。当 index 小于 0 时，它指定从末尾开始的索引，-1 是最后一个元素。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| tableIndex | int | 表的索引。 |
| rowIndex | int | 表中行的索引。 |

**退货:**
[Row](../../com.aspose.words/row) - 刚刚删除的行节点。
### endBookmark(String bookmarkName) {#endBookmark-java.lang.String-}
```
public BookmarkEnd endBookmark(String bookmarkName)
```


将文档中的当前位置标记为书签结束。

文档中的书签可以重叠并跨越任何范围。要创建有效的书签，您需要同时调用[startBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#startBookmark-java.lang.String-)和[endBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#endBookmark-java.lang.String-)同**bookmarkName**范围。

保存文档时将忽略格式错误的书签或具有重复名称的书签。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkName | java.lang.String | 书签的名称。 |

**退货:**
[BookmarkEnd](../../com.aspose.words/bookmarkend) - 刚刚创建的书签结束节点。
### endColumnBookmark(String bookmarkName) {#endColumnBookmark-java.lang.String-}
```
public BookmarkEnd endColumnBookmark(String bookmarkName)
```


将文档中的当前位置标记为列书签结束。该位置必须在表格单元格中。

列书签涵盖一系列行中的一个或多个列。要创建有效的书签，您需要同时调用[startColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#startColumnBookmark-java.lang.String-)和[endColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#endColumnBookmark-java.lang.String-)同**bookmarkName**范围。

保存文档时将忽略格式错误的书签或具有重复名称的书签。

插入的实际位置[BookmarkEnd](../../com.aspose.words/bookmarkend)节点可能与当前文档构建器位置不同。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkName | java.lang.String | 书签的名称。 |

**退货:**
[BookmarkEnd](../../com.aspose.words/bookmarkend) - 刚刚创建的书签结束节点。
### endEditableRange() {#endEditableRange--}
```
public EditableRangeEnd endEditableRange()
```


将文档中的当前位置标记为可编辑范围结束。

文档中的可编辑范围可以重叠并跨越任何范围。要创建有效的可编辑范围，您需要同时调用[startEditableRange()](../../com.aspose.words/documentbuilder\#startEditableRange--)和[endEditableRange()](../../com.aspose.words/documentbuilder\#endEditableRange--)或者[endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder\#endEditableRange-com.aspose.words.EditableRangeStart-)方法。

保存文档时将忽略格式错误的可编辑范围。

**退货:**
[EditableRangeEnd](../../com.aspose.words/editablerangeend) 刚刚创建的可编辑范围结束节点。
### endEditableRange(EditableRangeStart start) {#endEditableRange-com.aspose.words.EditableRangeStart-}
```
public EditableRangeEnd endEditableRange(EditableRangeStart start)
```


将文档中的当前位置标记为可编辑范围结束。

在创建嵌套的可编辑范围期间使用此重载。

文档中的可编辑范围可以重叠并跨越任何范围。要创建有效的可编辑范围，您需要同时调用[startEditableRange()](../../com.aspose.words/documentbuilder\#startEditableRange--)和[endEditableRange()](../../com.aspose.words/documentbuilder\#endEditableRange--)或者[endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder\#endEditableRange-com.aspose.words.EditableRangeStart-)方法。

保存文档时将忽略格式错误的可编辑范围。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| start | [EditableRangeStart](../../com.aspose.words/editablerangestart) | 此可编辑范围开始。 |

**退货:**
[EditableRangeEnd](../../com.aspose.words/editablerangeend) 刚刚创建的可编辑范围结束节点。
### endRow() {#endRow--}
```
public Row endRow()
```


结束文档中的表格行。

称呼**EndRow**结束表格行。如果你打电话[insertCell()](../../com.aspose.words/documentbuilder\#insertCell--)紧随其后，表格将在新行上继续。

使用[getRowFormat()](../../com.aspose.words/documentbuilder\#getRowFormat--)属性来指定行格式。

**退货:**
[Row](../../com.aspose.words/row) - 刚刚完成的行节点。
### endTable() {#endTable--}
```
public Table endTable()
```


结束文档中的表格。

此方法应仅在之后调用一次[endRow()](../../com.aspose.words/documentbuilder\#endRow--)被称为。调用时，**EndTable**将光标移出当前单元格，指向表格之后。

**退货:**
[Table](../../com.aspose.words/table) - 刚刚完成的表节点。
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
### fetchCellAttr(int key) {#fetchCellAttr-int-}
```
public Object fetchCellAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### fetchInheritedCellAttr(int key) {#fetchInheritedCellAttr-int-}
```
public Object fetchInheritedCellAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### fetchInheritedRowAttr(int key) {#fetchInheritedRowAttr-int-}
```
public Object fetchInheritedRowAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### fetchInheritedRunAttr(int fontAttr) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int fontAttr)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontAttr | int |  |

**退货:**
java.lang.Object
### fetchRowAttr(int key) {#fetchRowAttr-int-}
```
public Object fetchRowAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getBold() {#getBold--}
```
public boolean getBold()
```


如果字体格式为粗体，则为真。

**退货:**
boolean - 对应的布尔值。
### getCellFormat() {#getCellFormat--}
```
public CellFormat getCellFormat()
```


返回表示当前表格单元格格式化属性的对象。

**退货:**
[CellFormat](../../com.aspose.words/cellformat) - 表示当前表格单元格格式属性的对象。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getCurrentNode() {#getCurrentNode--}
```
public Node getCurrentNode()
```


获取当前在此 DocumentBuilder 中选择的节点。

**CurrentNode**是一个游标**DocumentBuilder**并指向一个**Node**那是一个的直接孩子**Paragraph**.您使用的任何插入操作**DocumentBuilder**将插入之前**CurrentNode**.

当前段落为空或光标位于段落结尾或结构化文档标记之前时，**CurrentNode**返回空值。

**退货:**
[Node](../../com.aspose.words/node) 当前在此 DocumentBuilder 中选择的节点。
### getCurrentParagraph() {#getCurrentParagraph--}
```
public Paragraph getCurrentParagraph()
```


获取当前在此 DocumentBuilder 中选择的段落。[getCurrentNode()](../../com.aspose.words/documentbuilder\#getCurrentNode--)

**退货:**
[Paragraph](../../com.aspose.words/paragraph) - 当前在此 DocumentBuilder 中选择的段落。
### getCurrentSection() {#getCurrentSection--}
```
public Section getCurrentSection()
```


获取当前在此 DocumentBuilder 中选择的部分。

**退货:**
[Section](../../com.aspose.words/section) - 当前在此 DocumentBuilder 中选择的部分。
### getCurrentStory() {#getCurrentStory--}
```
public Story getCurrentStory()
```


获取当前在此 DocumentBuilder 中选择的故事。

**退货:**
[Story](../../com.aspose.words/story) - 当前在此 DocumentBuilder 中选择的故事。
### getCurrentStructuredDocumentTag() {#getCurrentStructuredDocumentTag--}
```
public StructuredDocumentTag getCurrentStructuredDocumentTag()
```


获取当前在此 DocumentBuilder 中选择的结构化文档标记。

**退货:**
[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) - 当前在此 DocumentBuilder 中选择的结构化文档标签。
### getDirectCellAttr(int key) {#getDirectCellAttr-int-}
```
public Object getDirectCellAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getDirectRowAttr(int key) {#getDirectRowAttr-int-}
```
public Object getDirectRowAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getDirectRunAttr(int fontAttr) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int fontAttr)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontAttr | int |  |

**退货:**
java.lang.Object
### getDocument() {#getDocument--}
```
public Document getDocument()
```


获取[getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-)该对象附加到的对象。

**退货:**
[Document](../../com.aspose.words/document) - 这[getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-)该对象附加到的对象。
### getFont() {#getFont--}
```
public Font getFont()
```


返回表示当前字体格式属性的对象。

利用**Font**访问和修改字体格式属性。

在插入文本之前指定字体格式。

**退货:**
[Font](../../com.aspose.words/font) - 表示当前字体格式属性的对象。
### getItalic() {#getItalic--}
```
public boolean getItalic()
```


如果字体格式为斜体，则为真。

**退货:**
boolean - 对应的布尔值。
### getListFormat() {#getListFormat--}
```
public ListFormat getListFormat()
```


返回表示当前列表格式属性的对象。

**退货:**
[ListFormat](../../com.aspose.words/listformat) - 表示当前列表格式属性的对象。
### getPageSetup() {#getPageSetup--}
```
public PageSetup getPageSetup()
```


返回表示当前页面设置和部分属性的对象。

**退货:**
[PageSetup](../../com.aspose.words/pagesetup) - 表示当前页面设置和部分属性的对象。
### getParagraphFormat() {#getParagraphFormat--}
```
public ParagraphFormat getParagraphFormat()
```


返回表示当前段落格式属性的对象。

**退货:**
[ParagraphFormat](../../com.aspose.words/paragraphformat) - 表示当前段落格式属性的对象。
### getRowFormat() {#getRowFormat--}
```
public RowFormat getRowFormat()
```


返回表示当前表行格式设置属性的对象。

**退货:**
[RowFormat](../../com.aspose.words/rowformat) - 表示当前表格行格式属性的对象。
### getUnderline() {#getUnderline--}
```
public int getUnderline()
```


获取/设置当前字体的下划线类型。

**退货:**
int - 对应的 int 值。返回值是以下之一[Underline](../../com.aspose.words/underline)常数。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### insertBreak(int breakType) {#insertBreak-int-}
```
public void insertBreak(int breakType)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| breakType | int |  |

### insertCell() {#insertCell--}
```
public Cell insertCell()
```


在文档中插入表格单元格。

要开始一个表，只需调用**InsertCell**.在此之后，您使用其他方法添加的任何内容[DocumentBuilder](../../com.aspose.words/documentbuilder)类将被添加到当前单元格。

要在同一行中开始一个新单元格，请调用**InsertCell**再次。

结束表格行调用[endRow()](../../com.aspose.words/documentbuilder\#endRow--).

使用[getCellFormat()](../../com.aspose.words/documentbuilder\#getCellFormat--)属性来指定单元格格式。

**退货:**
[Cell](../../com.aspose.words/cell) - 刚刚插入的单元节点。
### insertChart(int chartType, double width, double height) {#insertChart-int-double-double-}
```
public Shape insertChart(int chartType, double width, double height)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| chartType | int |  |
| width | double |  |
| height | double |  |

**退货:**
[Shape](../../com.aspose.words/shape)
### insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertChart-int-int-double-int-double-double-double-int-}
```
public Shape insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| chartType | int |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| width | double |  |
| height | double |  |
| wrapType | int |  |

**退货:**
[Shape](../../com.aspose.words/shape)
### insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size) {#insertCheckBox-java.lang.String-boolean-boolean-int-}
```
public FormField insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size)
```


在当前位置插入一个复选框表单域。

如果您为表单域指定名称，则会自动创建具有相同名称的书签。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 表单域的名称。可以是空字符串。超过 20 个字符的值将被截断。 |
| defaultValue | boolean | 复选框表单字段的默认值。 |
| checkedValue | boolean | 复选框表单字段的当前选中状态。 |
| size | int | 以磅为单位指定复选框的大小。为 MS Word 指定 0 以自动计算复选框的大小。 |

**退货:**
[FormField](../../com.aspose.words/formfield) - 刚刚插入的表单域节点。
### insertCheckBox(String name, boolean checkedValue, int size) {#insertCheckBox-java.lang.String-boolean-int-}
```
public FormField insertCheckBox(String name, boolean checkedValue, int size)
```


在当前位置插入一个复选框表单域。

如果您为表单域指定名称，则会自动创建具有相同名称的书签。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 表单域的名称。可以是空字符串。超过 20 个字符的值将被截断。 |
| checkedValue | boolean | 检查复选框表单字段的状态。 |
| size | int | 以磅为单位指定复选框的大小。为 MS Word 指定 0 以自动计算复选框的大小。 |

**退货:**
[FormField](../../com.aspose.words/formfield) - 刚刚插入的表单域节点。
### insertComboBox(String name, String[] items, int selectedIndex) {#insertComboBox-java.lang.String-java.lang.String---int-}
```
public FormField insertComboBox(String name, String[] items, int selectedIndex)
```


在当前位置插入一个组合框表单域。

如果您为表单域指定名称，则会自动创建具有相同名称的书签。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 表单域的名称。可以是空字符串。超过 20 个字符的值将被截断。 |
| items | java.lang.String[] | ComboBox 的项目。最多为 25 个项目。 |
| selectedIndex | int | 组合框中所选项目的索引。 |

**退货:**
[FormField](../../com.aspose.words/formfield) - 刚刚插入的表单域节点。
### insertDocument(Document srcDoc, int importFormatMode) {#insertDocument-com.aspose.words.Document-int-}
```
public Node insertDocument(Document srcDoc, int importFormatMode)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document) |  |
| importFormatMode | int |  |

**退货:**
[Node](../../com.aspose.words/node)
### insertDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#insertDocument-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions-}
```
public Node insertDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions) |  |

**退货:**
[Node](../../com.aspose.words/node)
### insertField(int fieldType, boolean updateField) {#insertField-int-boolean-}
```
public Field insertField(int fieldType, boolean updateField)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldType | int |  |
| updateField | boolean |  |

**退货:**
[Field](../../com.aspose.words/field)
### insertField(String fieldCode) {#insertField-java.lang.String-}
```
public Field insertField(String fieldCode)
```


将 Word 域插入到文档中。将 Word 字段插入文档并更新字段结果。

此方法将字段插入文档并立即更新字段结果。 Aspose.Words 可以更新大多数类型的字段，但不是全部。有关更多详细信息，请参阅[insertField(java.lang.String, java.lang.String)](../../com.aspose.words/documentbuilder\#insertField-java.lang.String--java.lang.String-)超载。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | java.lang.String | 要插入的域代码（不带花括号）。 |

**退货:**
[Field](../../com.aspose.words/field) - 一个[Field](../../com.aspose.words/field)表示插入字段的对象。
### insertField(String fieldCode, String fieldValue) {#insertField-java.lang.String-java.lang.String-}
```
public Field insertField(String fieldCode, String fieldValue)
```


将 Word 字段插入文档而不更新字段结果。

Microsoft Word 文档中的字段由字段代码和字段结果组成。字段代码就像一个公式，字段结果就像公式产生的值。域代码还可能包含域开关，类似于执行特定操作的附加指令。

您可以使用键盘快捷键 Alt+F9 在 Microsoft Word 文档中显示域代码和结果之间切换。字段代码出现在大括号 (\ {\}）。

要创建字段，您需要指定字段类型、字段代码和“占位符”字段值。如果您不确定特定的域代码语法，请先在 Microsoft Word 中创建该域，然后切换以查看其域代码。

 Aspose.Words 可以计算大部分字段类型的字段结果，但是这种方法不会自动更新字段结果。由于字段结果不是自动计算的，因此您需要传递一些将插入到字段结果中的字符串值（甚至是空字符串）。该值将作为占位符保留在字段结果中，直到字段更新。要更新字段结果，您可以调用[Field.update()](../../com.aspose.words/field\#update--)在返回给您的字段对象上或[Document.update字段()](../../com.aspose.words/document\#update字段--)更新整个文档中的字段。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | java.lang.String | 要插入的域代码（不带花括号）。 |
| fieldValue | java.lang.String | 要插入的字段值。为没有值的字段传递 null。 |

**退货:**
[Field](../../com.aspose.words/field) - 一个[Field](../../com.aspose.words/field)表示插入字段的对象。
### insertFootnote(int footnoteType, String footnoteText) {#insertFootnote-int-java.lang.String-}
```
public Footnote insertFootnote(int footnoteType, String footnoteText)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| footnoteType | int |  |
| footnoteText | java.lang.String |  |

**退货:**
[Footnote](../../com.aspose.words/footnote)
### insertFootnote(int footnoteType, String footnoteText, String referenceMark) {#insertFootnote-int-java.lang.String-java.lang.String-}
```
public Footnote insertFootnote(int footnoteType, String footnoteText, String referenceMark)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| footnoteType | int |  |
| footnoteText | java.lang.String |  |
| referenceMark | java.lang.String |  |

**退货:**
[Footnote](../../com.aspose.words/footnote)
### insertHorizontalRule() {#insertHorizontalRule--}
```
public Shape insertHorizontalRule()
```


在文档中插入水平线形状。

**退货:**
[Shape](../../com.aspose.words/shape) - 水平规则的形状。
### insertHtml(String html) {#insertHtml-java.lang.String-}
```
public void insertHtml(String html)
```


将 HTML 字符串插入到文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| html | java.lang.String | 要插入到文档中的 HTML 字符串。您可以使用此方法插入 HTML 片段或整个 HTML 文档。 |

### insertHtml(String html, boolean useBuilderFormatting) {#insertHtml-java.lang.String-boolean-}
```
public void insertHtml(String html, boolean useBuilderFormatting)
```


将 HTML 字符串插入到文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| html | java.lang.String | 要插入到文档中的 HTML 字符串。 |
| useBuilderFormatting | boolean | 一个值，指示是否在[DocumentBuilder](../../com.aspose.words/documentbuilder)用作从 HTML 导入的文本的基本格式。

您可以使用此方法插入 HTML 片段或整个 HTML 文档。

当 useBuilderFormatting 为 false 时，[DocumentBuilder](../../com.aspose.words/documentbuilder)格式被忽略，插入文本的格式基于默认的 HTML 格式。因此，文本看起来就像在浏览器中呈现的一样。

当 useBuilderFormatting 为 true 时，插入文本的格式基于[DocumentBuilder](../../com.aspose.words/documentbuilder)格式，并且文本看起来好像是插入的[write(java.lang.String)](../../com.aspose.words/documentbuilder\#write-java.lang.String-). |

### insertHtml(String html, int options) {#insertHtml-java.lang.String-int-}
```
public void insertHtml(String html, int options)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| html | java.lang.String |  |
| options | int |  |

### insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark) {#insertHyperlink-java.lang.String-java.lang.String-boolean-}
```
public Field insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark)
```


在文档中插入超链接。

请注意，您需要使用显式指定超链接显示文本的字体格式[getFont()](../../com.aspose.words/documentbuilder\#getFont--)财产。

此方法在内部调用[insertField(java.lang.String)](../../com.aspose.words/documentbuilder\#insertField-java.lang.String-)在文档中插入一个 MS Word HYPERLINK 字段。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| displayText | java.lang.String | 要在文档中显示的链接的文本。 |
| urlOrBookmark | java.lang.String | 链接目的地。可以是文档中的 url 或书签的名称。此方法总是在 url 的开头和结尾添加撇号。 |
| isBookmark | boolean | 如果前一个参数是文档中书签的名称，则为真； false 是前面的参数是一个 URL。 |

**退货:**
[Field](../../com.aspose.words/field) - 一个[Field](../../com.aspose.words/field)表示插入字段的对象。
### insertImage(byte[] imageBytes) {#insertImage-byte---}
```
public Shape insertImage(byte[] imageBytes)
```


将字节数组中的图像插入到文档中。图像以 100% 的比例内嵌插入。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| imageBytes | byte[] | 包含图像的字节数组。 |

**退货:**
[Shape](../../com.aspose.words/shape) - 刚刚插入的图像节点。

您可以使用[Shape](../../com.aspose.words/shape)此方法返回的对象。
### insertImage(byte[] imageBytes, double width, double height) {#insertImage-byte---double-double-}
```
public Shape insertImage(byte[] imageBytes, double width, double height)
```


将字节数组中的内联图像插入文档并将其缩放到指定大小。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| imageBytes | byte[] | 包含图像的字节数组。 |
| width | double | 图像的宽度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |
| height | double | 图像的高度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |

**退货:**
[Shape](../../com.aspose.words/shape) - 刚刚插入的图像节点。

您可以使用[Shape](../../com.aspose.words/shape)此方法返回的对象。
### insertImage(byte[] imageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-byte---int-double-int-double-double-double-int-}
```
public Shape insertImage(byte[] imageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| imageBytes | byte[] |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| width | double |  |
| height | double |  |
| wrapType | int |  |

**退货:**
[Shape](../../com.aspose.words/shape)
### insertImage(BufferedImage image) {#insertImage-java.awt.image.BufferedImage-}
```
public Shape insertImage(BufferedImage image)
```


在文档中插入图像。将对象中的图像插入到文档中。图像以 100% 的比例内嵌插入。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | 要插入到文档中的图像。 |

**退货:**
[Shape](../../com.aspose.words/shape) - 刚刚插入的图像节点。

您可以使用[Shape](../../com.aspose.words/shape)此方法返回的对象。

Aspose.Words 将以 PNG 格式和默认设置插入图像。如果要插入另一种格式或其他设置的 BufferedImage，则需要将图像保存到字节数组中并使用[insertImage(byte[])](../../com.aspose.words/documentbuilder\#insertImage-byte---).
### insertImage(BufferedImage image, double width, double height) {#insertImage-java.awt.image.BufferedImage-double-double-}
```
public Shape insertImage(BufferedImage image, double width, double height)
```


将来自对象的内嵌图像插入到文档中并将其缩放到指定的大小。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | 要插入到文档中的图像。 |
| width | double | 图像的宽度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |
| height | double | 图像的高度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |

**退货:**
[Shape](../../com.aspose.words/shape) - 刚刚插入的图像节点。

您可以使用[Shape](../../com.aspose.words/shape)此方法返回的对象。

Aspose.Words 将以 PNG 格式和默认设置插入图像。如果要插入另一种格式或其他设置的 BufferedImage，则需要将图像保存到字节数组中并使用[insertImage(byte[])](../../com.aspose.words/documentbuilder\#insertImage-byte---).
### insertImage(BufferedImage image, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.awt.image.BufferedImage-int-double-int-double-double-double-int-}
```
public Shape insertImage(BufferedImage image, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| image | java.awt.image.BufferedImage |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| width | double |  |
| height | double |  |
| wrapType | int |  |

**退货:**
[Shape](../../com.aspose.words/shape)
### insertImage(InputStream stream) {#insertImage-java.io.InputStream-}
```
public Shape insertImage(InputStream stream)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.InputStream |  |

**退货:**
[Shape](../../com.aspose.words/shape)
### insertImage(InputStream stream, double width, double height) {#insertImage-java.io.InputStream-double-double-}
```
public Shape insertImage(InputStream stream, double width, double height)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| width | double |  |
| height | double |  |

**退货:**
[Shape](../../com.aspose.words/shape)
### insertImage(InputStream stream, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.io.InputStream-int-double-int-double-double-double-int-}
```
public Shape insertImage(InputStream stream, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| width | double |  |
| height | double |  |
| wrapType | int |  |

**退货:**
[Shape](../../com.aspose.words/shape)
### insertImage(String fileName) {#insertImage-java.lang.String-}
```
public Shape insertImage(String fileName)
```


将文件或 URL 中的图像插入到文档中。图像以 100% 的比例内嵌插入。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 带有图像的文件。可以是任何有效的本地或远程 URI。 |

**退货:**
[Shape](../../com.aspose.words/shape) - 刚刚插入的图像节点。

如果您指定远程 URI，此重载将在插入文档之前自动下载图像。

您可以使用[Shape](../../com.aspose.words/shape)此方法返回的对象。
### insertImage(String fileName, double width, double height) {#insertImage-java.lang.String-double-double-}
```
public Shape insertImage(String fileName, double width, double height)
```


将文件或 URL 中的内联图像插入到文档中，并将其缩放到指定的大小。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 包含图像的文件。 |
| width | double | 图像的宽度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |
| height | double | 图像的高度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |

**退货:**
[Shape](../../com.aspose.words/shape) - 刚刚插入的图像节点。

您可以使用[Shape](../../com.aspose.words/shape)此方法返回的对象。
### insertImage(String fileName, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.lang.String-int-double-int-double-double-double-int-}
```
public Shape insertImage(String fileName, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| width | double |  |
| height | double |  |
| wrapType | int |  |

**退货:**
[Shape](../../com.aspose.words/shape)
### insertNode(Node node) {#insertNode-com.aspose.words.Node-}
```
public void insertNode(Node node)
```


在光标前插入一个节点。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) |  |

### insertOleObject(InputStream stream, String progId, boolean asIcon, InputStream presentation) {#insertOleObject-java.io.InputStream-java.lang.String-boolean-java.io.InputStream-}
```
public Shape insertOleObject(InputStream stream, String progId, boolean asIcon, InputStream presentation)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| progId | java.lang.String |  |
| asIcon | boolean |  |
| presentation | java.io.InputStream |  |

**退货:**
[Shape](../../com.aspose.words/shape)
### insertOleObject(String fileName, boolean isLinked, boolean asIcon, InputStream presentation) {#insertOleObject-java.lang.String-boolean-boolean-java.io.InputStream-}
```
public Shape insertOleObject(String fileName, boolean isLinked, boolean asIcon, InputStream presentation)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String |  |
| isLinked | boolean |  |
| asIcon | boolean |  |
| presentation | java.io.InputStream |  |

**退货:**
[Shape](../../com.aspose.words/shape)
### insertOleObject(String fileName, String progId, boolean isLinked, boolean asIcon, InputStream presentation) {#insertOleObject-java.lang.String-java.lang.String-boolean-boolean-java.io.InputStream-}
```
public Shape insertOleObject(String fileName, String progId, boolean isLinked, boolean asIcon, InputStream presentation)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String |  |
| progId | java.lang.String |  |
| isLinked | boolean |  |
| asIcon | boolean |  |
| presentation | java.io.InputStream |  |

**退货:**
[Shape](../../com.aspose.words/shape)
### insertOleObjectAsIcon(InputStream stream, String progId, String iconFile, String iconCaption) {#insertOleObjectAsIcon-java.io.InputStream-java.lang.String-java.lang.String-java.lang.String-}
```
public Shape insertOleObjectAsIcon(InputStream stream, String progId, String iconFile, String iconCaption)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| progId | java.lang.String |  |
| iconFile | java.lang.String |  |
| iconCaption | java.lang.String |  |

**退货:**
[Shape](../../com.aspose.words/shape)
### insertOleObjectAsIcon(String fileName, boolean isLinked, String iconFile, String iconCaption) {#insertOleObjectAsIcon-java.lang.String-boolean-java.lang.String-java.lang.String-}
```
public Shape insertOleObjectAsIcon(String fileName, boolean isLinked, String iconFile, String iconCaption)
```


将嵌入或链接的 OLE 对象作为图标插入到文档中。允许指定图标文件和标题。使用文件扩展名检测 OLE 对象类型。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 文件的完整路径。 |
| isLinked | boolean | 如果为真，则插入链接的 OLE 对象，否则插入嵌入的 OLE 对象。 |
| iconFile | java.lang.String | ICO 文件的完整路径。如果值为 null，Aspose.Words 将使用预定义的图像。 |
| iconCaption | java.lang.String | 图标标题。如果值为 null，Aspose.Words 将使用文件名。 |

**退货:**
[Shape](../../com.aspose.words/shape) 包含 Ole 对象并插入到当前构建器位置的形状节点。
### insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption) {#insertOleObjectAsIcon-java.lang.String-java.lang.String-boolean-java.lang.String-java.lang.String-}
```
public Shape insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption)
```


将嵌入或链接的 OLE 对象作为图标插入到文档中。允许指定图标文件和标题。使用给定的 progID 参数检测 OLE 对象类型。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 文件的完整路径。 |
| progId | java.lang.String | OLE 对象的 ProgId。 |
| isLinked | boolean | 如果为真，则插入链接的 OLE 对象，否则插入嵌入的 OLE 对象。 |
| iconFile | java.lang.String | ICO 文件的完整路径。如果值为 null，Aspose.Words 将使用预定义的图像。 |
| iconCaption | java.lang.String | 图标标题。如果值为 null，Aspose.Words 将使用文件名。 |

**退货:**
[Shape](../../com.aspose.words/shape) 包含 Ole 对象并插入到当前构建器位置的形状节点。
### insertOnlineVideo(String videoUrl, double width, double height) {#insertOnlineVideo-java.lang.String-double-double-}
```
public Shape insertOnlineVideo(String videoUrl, double width, double height)
```


将在线视频对象插入文档并将其缩放到指定大小。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| videoUrl | java.lang.String | 视频的 URL。 |
| width | double | 图像的宽度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |
| height | double | 图像的高度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |

**退货:**
[Shape](../../com.aspose.words/shape) - 刚刚插入的图像节点。

您可以使用[Shape](../../com.aspose.words/shape)此方法返回的对象。

支持从以下资源插入在线视频：

 *  https://www.youtube.com/
 *  https://vimeo.com/

如果您的在线视频显示不正确，请使用[insertOnlineVideo(java.lang.String, java.lang.String, byte[], double, double)](../../com.aspose.words/documentbuilder\#insertOnlineVideo-java.lang.String--java.lang.String--byte----double--double-)，它接受自定义的嵌入式 html 代码。

嵌入视频的代码可能因提供商而异，请咨询您选择的相应提供商以了解详细信息。
### insertOnlineVideo(String videoUrl, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertOnlineVideo-java.lang.String-int-double-int-double-double-double-int-}
```
public Shape insertOnlineVideo(String videoUrl, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| videoUrl | java.lang.String |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| width | double |  |
| height | double |  |
| wrapType | int |  |

**退货:**
[Shape](../../com.aspose.words/shape)
### insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height) {#insertOnlineVideo-java.lang.String-java.lang.String-byte---double-double-}
```
public Shape insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height)
```


将在线视频对象插入文档并将其缩放到指定大小。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| videoUrl | java.lang.String | 视频的 URL。 |
| videoEmbedCode | java.lang.String | 视频的嵌入代码。 |
| thumbnailImageBytes | byte[] | 缩略图图像字节。 |
| width | double | 图像的宽度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |
| height | double | 图像的高度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |

**退货:**
[Shape](../../com.aspose.words/shape) - 刚刚插入的图像节点。

您可以使用[Shape](../../com.aspose.words/shape)此方法返回的对象。
### insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertOnlineVideo-java.lang.String-java.lang.String-byte---int-double-int-double-double-double-int-}
```
public Shape insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| videoUrl | java.lang.String |  |
| videoEmbedCode | java.lang.String |  |
| thumbnailImageBytes | byte[] |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| width | double |  |
| height | double |  |
| wrapType | int |  |

**退货:**
[Shape](../../com.aspose.words/shape)
### insertParagraph() {#insertParagraph--}
```
public Paragraph insertParagraph()
```


在文档中插入段落分隔符。

指定的当前段落格式[getParagraphFormat()](../../com.aspose.words/documentbuilder\#getParagraphFormat--)财产被使用。

将当前段落一分为二。插入段落后，光标位于新段落的开头。

**退货:**
[Paragraph](../../com.aspose.words/paragraph) 刚刚插入的段落节点。它是同一个节点[getCurrentParagraph()](../../com.aspose.words/documentbuilder\#getCurrentParagraph--).
### insertShape(int shapeType, double width, double height) {#insertShape-int-double-double-}
```
public Shape insertShape(int shapeType, double width, double height)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| shapeType | int |  |
| width | double |  |
| height | double |  |

**退货:**
[Shape](../../com.aspose.words/shape)
### insertShape(int shapeType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertShape-int-int-double-int-double-double-double-int-}
```
public Shape insertShape(int shapeType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| shapeType | int |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| width | double |  |
| height | double |  |
| wrapType | int |  |

**退货:**
[Shape](../../com.aspose.words/shape)
### insertSignatureLine(SignatureLineOptions signatureLineOptions) {#insertSignatureLine-com.aspose.words.SignatureLineOptions-}
```
public Shape insertSignatureLine(SignatureLineOptions signatureLineOptions)
```


在当前位置插入签名行。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| signatureLineOptions | [SignatureLineOptions](../../com.aspose.words/signaturelineoptions) | 存储创建签名行参数的对象。 |

**退货:**
[Shape](../../com.aspose.words/shape) - 刚刚插入的签名行节点。
### insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType) {#insertSignatureLine-com.aspose.words.SignatureLineOptions-int-double-int-double-int-}
```
public Shape insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| signatureLineOptions | [SignatureLineOptions](../../com.aspose.words/signaturelineoptions) |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| wrapType | int |  |

**退货:**
[Shape](../../com.aspose.words/shape)
### insertStyleSeparator() {#insertStyleSeparator--}
```
public void insertStyleSeparator()
```


将样式分隔符插入文档。此方法允许将不同的段落样式应用于文本行的两个不同部分。

### insertTableOfContents(String switches) {#insertTableOfContents-java.lang.String-}
```
public Field insertTableOfContents(String switches)
```


在文档中插入一个 TOC（目录）字段。

此方法将 TOC（目录）字段插入文档的当前位置。

可以通过多种方式构建 Word 文档中的目录，并使用多种选项设置其格式。 Microsoft Word 创建和显示表格的方式由字段开关控制。

指定开关的最简单方法是使用“插入”->“参考”->“索引和表格”菜单将目录插入和配置到 Word 文档中，然后打开域代码显示以查看开关。您可以在 Microsoft Word 中按 Alt+F9 来打开或关闭域代码的显示。

例如，在创建目录后，将以下字段插入到文档中：**\{ TOC \\o "1-3" \\h \\z \}** .你可以复制**\\o "1-3" \\h \\z**并将其用作开关参数。

注意**InsertTableOfContents**只会插入一个 TOC 字段，但不会实际构建目录。目录是在字段更新时由 Microsoft Word 构建的。

如果使用此方法插入目录，然后在 Microsoft Word 中打开文件，您将看不到目录，因为 TOC 字段尚未更新。

在 Microsoft Word 中，打开文档时不会自动更新字段，但您可以随时按 F9 键更新文档中的字段。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| switches | java.lang.String | TOC 字段切换。 |

**退货:**
[Field](../../com.aspose.words/field)
### insertTextInput(String name, int type, String format, String fieldValue, int maxLength) {#insertTextInput-java.lang.String-int-java.lang.String-java.lang.String-int-}
```
public FormField insertTextInput(String name, int type, String format, String fieldValue, int maxLength)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String |  |
| type | int |  |
| format | java.lang.String |  |
| fieldValue | java.lang.String |  |
| maxLength | int |  |

**退货:**
[FormField](../../com.aspose.words/formfield)
### isAtEndOfParagraph() {#isAtEndOfParagraph--}
```
public boolean isAtEndOfParagraph()
```


如果光标位于当前段落的末尾，则返回 true。

**退货:**
boolean - 如果光标位于当前段落的末尾则为真。
### isAtEndOfStructuredDocumentTag() {#isAtEndOfStructuredDocumentTag--}
```
public boolean isAtEndOfStructuredDocumentTag()
```


退货**true**如果光标位于结构化文档标签的末尾。

**退货:**
布尔值 -**true**如果光标位于结构化文档标签的末尾。
### isAtStartOfParagraph() {#isAtStartOfParagraph--}
```
public boolean isAtStartOfParagraph()
```


如果光标位于当前段落的开头（光标前没有文本），则返回 true。

**退货:**
boolean - 如果光标位于当前段落的开头（光标前没有文本），则为 True。
### moveTo(Node node) {#moveTo-com.aspose.words.Node-}
```
public void moveTo(Node node)
```


将光标移动到内联节点或段落末尾。

什么时候*node*是一个内联级节点，光标移动到这个节点，更多的内容将被插入到那个节点之前。

什么时候*node*是一个**Paragraph**光标移动到段落末尾，更多内容将插入到段落分隔符之前。

什么时候*node*是块级节点但不是段落，光标将移动到第一段的末尾进入块级节点，并且将在段落中断之前插入更多内容。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) | 该节点必须是段落或段落的直接子节点。 |

### moveToBookmark(String bookmarkName) {#moveToBookmark-java.lang.String-}
```
public boolean moveToBookmark(String bookmarkName)
```


将光标移动到书签。

将光标移动到指定名称的书签开头之后的位置。

比较不区分大小写。如果没有找到书签，则返回 false 并且不移动光标。

插入新文本不会替换书签的现有文本。

请注意，文档中的某些书签已分配给表单域。移动到这样的书签并在那里插入文本会将文本插入到表单域代码中。虽然这不会使表单域无效，但插入的文本将不可见，因为它成为域代码的一部分。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkName | java.lang.String | 要将光标移动到的书签的名称。 |

**退货:**
boolean - 如果找到书签则为真；否则为假。
### moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter) {#moveToBookmark-java.lang.String-boolean-boolean-}
```
public boolean moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter)
```


以更高的精度将光标移动到书签。

将光标移动到书签开始或结束之前或之后的位置。

如果所需位置不在行内级别，则移至下一段。

比较不区分大小写。如果没有找到书签，则返回 false 并且不移动光标。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkName | java.lang.String | 要将光标移动到的书签的名称。 |
| isStart | boolean | 如果为 true，则将光标移动到书签的开头。如果为 false，则将光标移动到书签的末尾。 |
| isAfter | boolean | 如果为 true，则将光标移动到书签开始或结束位置之后。如果为 false，则将光标移动到书签开始或结束位置之前。 |

**退货:**
boolean - 如果找到书签则为真；否则为假。
### moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex) {#moveToCell-int-int-int-int-}
```
public void moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)
```


将光标移动到当前部分中的表格单元格。

导航在当前部分的当前故事内执行。

对于index参数，当index大于等于0时，指定从头开始的一个索引，0为第一个元素。当 index 小于 0 时，它指定从末尾开始的索引，-1 是最后一个元素。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| tableIndex | int | 要移动到的表的索引。 |
| rowIndex | int | 表中行的索引。 |
| columnIndex | int | 表中列的索引。 |
| characterIndex | int | 单元格内字符的索引。负值允许您指定从单元格末尾开始的位置。使用 -1 移动到单元格的末尾。 |

### moveToDocumentEnd() {#moveToDocumentEnd--}
```
public void moveToDocumentEnd()
```


将光标移动到文档的末尾。

### moveToDocumentStart() {#moveToDocumentStart--}
```
public void moveToDocumentStart()
```


将光标移动到文档的开头。

### moveToField(Field field, boolean isAfter) {#moveToField-com.aspose.words.Field-boolean-}
```
public void moveToField(Field field, boolean isAfter)
```


将光标移动到文档中的某个字段。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| field | [Field](../../com.aspose.words/field) | 要将光标移动到的字段。 |
| isAfter | boolean | 为真时，将光标移动到字段结束之后。当为假时，将光标移动到字段开始之前。 |

### moveToHeaderFooter(int headerFooterType) {#moveToHeaderFooter-int-}
```
public void moveToHeaderFooter(int headerFooterType)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| headerFooterType | int |  |

### moveToMergeField(String fieldName) {#moveToMergeField-java.lang.String-}
```
public boolean moveToMergeField(String fieldName)
```


将光标移动到指定的合并字段。将光标移动到刚好超出指定合并字段的位置并删除合并字段。

请注意，此方法会在移动光标后从文档中删除合并字段。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldName | java.lang.String | 邮件合并字段的名称不区分大小写。 |

**退货:**
boolean - 如果找到合并域并且移动光标则为真；否则为假。
### moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField) {#moveToMergeField-java.lang.String-boolean-boolean-}
```
public boolean moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField)
```


将合并字段移动到指定的合并字段。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldName | java.lang.String | 邮件合并字段的名称不区分大小写。 |
| isAfter | boolean | 为真时，将光标移动到字段结束之后。当为假时，将光标移动到字段开始之前。 |
| isDeleteField | boolean | 为真时，删除合并字段。 |

**退货:**
boolean - 如果找到合并域并且移动光标则为真；否则为假。
### moveToParagraph(int paragraphIndex, int characterIndex) {#moveToParagraph-int-int-}
```
public void moveToParagraph(int paragraphIndex, int characterIndex)
```


将光标移动到当前节中的段落。

导航在当前部分的当前故事中执行。也就是说，如果您将光标移动到第一部分的主标题，则 paragraphIndex 指定该部分标题内的段落索引。

当paragraphIndex 大于或等于0 时，它指定从section 开始的索引，0 是第一个段落。当paragraphIndex 小于0 时，它指定从节末尾开始的索引，-1 是最后一个段落。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| paragraphIndex | int | 要移动到的段落的索引。 |
| characterIndex | int | 段落内字符的索引。负值允许您指定从段落末尾开始的位置。使用 -1 移动到段落的末尾。 |

### moveToSection(int sectionIndex) {#moveToSection-int-}
```
public void moveToSection(int sectionIndex)
```


将光标移动到指定部分的正文开头。

当 sectionIndex 大于或等于 0 时，它指定从文档开头开始的索引，其中 0 为第一节。当 sectionIndex 小于 0 时，它指定从文档末尾开始的索引，-1 是最后一个部分。

光标移动到第一段**Body**的指定部分。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sectionIndex | int | 要移动到的部分的索引。 |

### moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex) {#moveToStructuredDocumentTag-com.aspose.words.StructuredDocumentTag-int-}
```
public void moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex)
```


将光标移动到结构化文档标签。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| structuredDocumentTag | [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) | 要移动到的结构化文档标签。 |
| characterIndex | int | 结构化文档标签内字符的索引。负值允许您指定从结构化文档标签末尾开始的位置。使用 -1 移动到结构化文档标签的末尾。如果结构化文档标记处于块级别，并且您要将光标移动到其最后一段的末尾，请指定 -2。 |

### moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex) {#moveToStructuredDocumentTag-int-int-}
```
public void moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```


将光标移动到当前部分中的结构化文档标签。

导航在当前部分的当前故事内执行。也就是说，如果您将光标移动到第一节的主标题，那么structuredDocumentTagIndex 指定了该节标题内的结构化文档标签的索引。

当structuredDocumentTagIndex 大于或等于0 时，它指定从节开头开始的索引，其中0 是第一个结构化文档标签。当structuredDocumentTagIndex 小于0 时，它指定从节末尾开始的索引，-1 是最后一个结构化文档标签。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| structuredDocumentTagIndex | int | 要移动到的结构化文档标签的索引。 |
| characterIndex | int | 结构化文档标签内字符的索引。负值允许您指定从结构化文档标签末尾开始的位置。使用 -1 移动到结构化文档标签的末尾。如果结构化文档标记处于块级别，并且您要将光标移动到其最后一段的末尾，请指定 -2。 |

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### popFont() {#popFont--}
```
public void popFont()
```


检索以前保存在堆栈中的字符格式。

### pushFont() {#pushFont--}
```
public void pushFont()
```


将当前字符格式保存到堆栈中。

### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

### resetToDefaultAttrs() {#resetToDefaultAttrs--}
```
public void resetToDefaultAttrs()
```




### setBold(boolean value) {#setBold-boolean-}
```
public void setBold(boolean value)
```


如果字体格式为粗体，则为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setCellAttr(int key, Object value) {#setCellAttr-int-java.lang.Object-}
```
public void setCellAttr(int key, Object value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setDocument(Document value) {#setDocument-com.aspose.words.Document-}
```
public void setDocument(Document value)
```


设置[getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-)该对象附加到的对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [Document](../../com.aspose.words/document) | 这[getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-)该对象附加到的对象。 |

### setItalic(boolean value) {#setItalic-boolean-}
```
public void setItalic(boolean value)
```


如果字体格式为斜体，则为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setRowAttr(int key, Object value) {#setRowAttr-int-java.lang.Object-}
```
public void setRowAttr(int key, Object value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setRunAttr(int fontAttr, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int fontAttr, Object value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontAttr | int |  |
| value | java.lang.Object |  |

### setUnderline(int value) {#setUnderline-int-}
```
public void setUnderline(int value)
```


获取/设置当前字体的下划线类型。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[Underline](../../com.aspose.words/underline)常数。 |

### startBookmark(String bookmarkName) {#startBookmark-java.lang.String-}
```
public BookmarkStart startBookmark(String bookmarkName)
```


将文档中的当前位置标记为书签开始。

文档中的书签可以重叠并跨越任何范围。要创建有效的书签，您需要同时调用[startBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#startBookmark-java.lang.String-)和[endBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#endBookmark-java.lang.String-)同**bookmarkName**范围。

保存文档时将忽略格式错误的书签或具有重复名称的书签。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkName | java.lang.String | 书签的名称。 |

**退货:**
[BookmarkStart](../../com.aspose.words/bookmarkstart) 刚刚创建的书签起始节点。
### startColumnBookmark(String bookmarkName) {#startColumnBookmark-java.lang.String-}
```
public BookmarkStart startColumnBookmark(String bookmarkName)
```


将文档中的当前位置标记为列书签开始。该位置必须在表格单元格中。

列书签涵盖一系列行中的一个或多个列。要创建有效的书签，您需要同时调用[startColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#startColumnBookmark-java.lang.String-)和[endColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#endColumnBookmark-java.lang.String-)同**bookmarkName**范围。

保存文档时将忽略格式错误的书签或具有重复名称的书签。

插入的实际位置[BookmarkStart](../../com.aspose.words/bookmarkstart)节点可能与当前文档构建器位置不同。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkName | java.lang.String | 书签的名称。 |

**退货:**
[BookmarkStart](../../com.aspose.words/bookmarkstart) 刚刚创建的书签起始节点。
### startEditableRange() {#startEditableRange--}
```
public EditableRangeStart startEditableRange()
```


将文档中的当前位置标记为可编辑范围的起点。

文档中的可编辑范围可以重叠并跨越任何范围。要创建有效的可编辑范围，您需要同时调用[startEditableRange()](../../com.aspose.words/documentbuilder\#startEditableRange--)和[endEditableRange()](../../com.aspose.words/documentbuilder\#endEditableRange--)或者[endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder\#endEditableRange-com.aspose.words.EditableRangeStart-)方法。

保存文档时将忽略格式错误的可编辑范围。

**退货:**
[EditableRangeStart](../../com.aspose.words/editablerangestart) - 刚刚创建的可编辑范围起始节点。
### startTable() {#startTable--}
```
public Table startTable()
```


在文档中开始一个表格。

下一个要调用的方法是[insertCell()](../../com.aspose.words/documentbuilder\#insertCell--).

当在单元格内调用时，此方法会启动一个嵌套表格。

**退货:**
[Table](../../com.aspose.words/table) - 刚刚创建的表节点。
### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
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

### write(String text) {#write-java.lang.String-}
```
public void write(String text)
```


在文档的当前插入位置插入一个字符串。指定的当前字体格式[getFont()](../../com.aspose.words/documentbuilder\#getFont--)财产被使用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| text | java.lang.String | 要插入到文档中的字符串。 |

### writeln() {#writeln--}
```
public void writeln()
```


在文档中插入段落分隔符。

来电[insertParagraph()](../../com.aspose.words/documentbuilder\#insertParagraph--).

### writeln(String text) {#writeln-java.lang.String-}
```
public void writeln(String text)
```


在文档中插入一个字符串和一个段落分隔符。指定的当前字体和段落格式[getFont()](../../com.aspose.words/documentbuilder\#getFont--)和[getParagraphFormat()](../../com.aspose.words/documentbuilder\#getParagraphFormat--)使用属性。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| text | java.lang.String | 要插入到文档中的字符串。 |
