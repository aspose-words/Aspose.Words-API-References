---
title: DocumentBuilder
second_title: Aspose.Words for Java API Reference
description: Provides methods to insert text images and other content specify font paragraph and section formatting.
type: docs
weight: 122
url: /java/com.aspose.words/documentbuilder/
---

**Inheritance:**
java.lang.Object
```
public class DocumentBuilder
```

Provides methods to insert text, images and other content, specify font, paragraph and section formatting.

To learn more, visit the **Document Builder Overview** documentation article.

**DocumentBuilder** makes the process of building a **Document** easier. **Document** is a composite object consisting of a tree of nodes and while inserting content nodes directly into the tree is possible, it requires good understanding of the tree structure. **DocumentBuilder** is a "facade" for the complex structure of **Document** and allows to insert content and formatting quickly and easily.

Create a **DocumentBuilder** and associate it with a [getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-).

The **DocumentBuilder** has an internal cursor where the text will be inserted when you call [write(java.lang.String)](../../com.aspose.words/documentbuilder\#write-java.lang.String-), [writeln(java.lang.String)](../../com.aspose.words/documentbuilder\#writeln-java.lang.String-), **M:Aspose.Words.DocumentBuilder.InsertBreak(Aspose.Words.BreakType)** and other methods. You can navigate the **DocumentBuilder** cursor to a different location in a document using various MoveToXXX methods.

Use the [getFont()](../../com.aspose.words/documentbuilder\#getFont--) property to specify character formatting that will apply to all text inserted from the current position in the document onwards.

Use the [getParagraphFormat()](../../com.aspose.words/documentbuilder\#getParagraphFormat--) property to specify paragraph formatting for the current and all paragraphs that will be inserted.

Use the [getPageSetup()](../../com.aspose.words/documentbuilder\#getPageSetup--) property to specify page and section properties for the current section and all section that will be inserted.

Use the [getCellFormat()](../../com.aspose.words/documentbuilder\#getCellFormat--) and [getRowFormat()](../../com.aspose.words/documentbuilder\#getRowFormat--) properties to specify formatting properties for table cells and rows. User the [insertCell()](../../com.aspose.words/documentbuilder\#insertCell--) and [endRow()](../../com.aspose.words/documentbuilder\#endRow--) methods to build a table.

Note that **Font**, **ParagraphFormat** and **PageSetup** properties are updated whenever you navigate to a different place in the document to reflect formatting properties available at the new location.
## Constructors

| Constructor | Description |
| --- | --- |
| [DocumentBuilder()](#DocumentBuilder--) | Initializes a new instance of this class. |
| [DocumentBuilder(Document doc)](#DocumentBuilder-com.aspose.words.Document-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [clearCellAttrs()](#clearCellAttrs--) |  |
| [clearRowAttrs()](#clearRowAttrs--) |  |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [deleteRow(int tableIndex, int rowIndex)](#deleteRow-int-int-) | Deletes a row from a table. |
| [endBookmark(String bookmarkName)](#endBookmark-java.lang.String-) | Marks the current position in the document as a bookmark end. |
| [endColumnBookmark(String bookmarkName)](#endColumnBookmark-java.lang.String-) | Marks the current position in the document as a column bookmark end. |
| [endEditableRange()](#endEditableRange--) | Marks the current position in the document as an editable range end. |
| [endEditableRange(EditableRangeStart start)](#endEditableRange-com.aspose.words.EditableRangeStart-) | Marks the current position in the document as an editable range end. |
| [endRow()](#endRow--) | Ends a table row in the document. |
| [endTable()](#endTable--) | Ends a table in the document. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchCellAttr(int key)](#fetchCellAttr-int-) |  |
| [fetchInheritedCellAttr(int key)](#fetchInheritedCellAttr-int-) |  |
| [fetchInheritedRowAttr(int key)](#fetchInheritedRowAttr-int-) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int-) |  |
| [fetchRowAttr(int key)](#fetchRowAttr-int-) |  |
| [getBold()](#getBold--) | True if the font is formatted as bold. |
| [getCellFormat()](#getCellFormat--) | Returns an object that represents current table cell formatting properties. |
| [getClass()](#getClass--) |  |
| [getCurrentNode()](#getCurrentNode--) | Gets the node that is currently selected in this DocumentBuilder. |
| [getCurrentParagraph()](#getCurrentParagraph--) | Gets the paragraph that is currently selected in this DocumentBuilder. |
| [getCurrentSection()](#getCurrentSection--) | Gets the section that is currently selected in this DocumentBuilder. |
| [getCurrentStory()](#getCurrentStory--) | Gets the story that is currently selected in this DocumentBuilder. |
| [getCurrentStructuredDocumentTag()](#getCurrentStructuredDocumentTag--) | Gets the structured document tag that is currently selected in this DocumentBuilder. |
| [getDirectCellAttr(int key)](#getDirectCellAttr-int-) |  |
| [getDirectRowAttr(int key)](#getDirectRowAttr-int-) |  |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int-) |  |
| [getDocument()](#getDocument--) | Gets the [getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-) object that this object is attached to. |
| [getFont()](#getFont--) | Returns an object that represents current font formatting properties. |
| [getItalic()](#getItalic--) | True if the font is formatted as italic. |
| [getListFormat()](#getListFormat--) | Returns an object that represents current list formatting properties. |
| [getPageSetup()](#getPageSetup--) | Returns an object that represents current page setup and section properties. |
| [getParagraphFormat()](#getParagraphFormat--) | Returns an object that represents current paragraph formatting properties. |
| [getRowFormat()](#getRowFormat--) | Returns an object that represents current table row formatting properties. |
| [getUnderline()](#getUnderline--) | Gets/sets underline type for the current font. |
| [hashCode()](#hashCode--) |  |
| [insertBreak(int breakType)](#insertBreak-int-) |  |
| [insertCell()](#insertCell--) | Inserts a table cell into the document. |
| [insertChart(int chartType, double width, double height)](#insertChart-int-double-double-) |  |
| [insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertChart-int-int-double-int-double-double-double-int-) |  |
| [insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size)](#insertCheckBox-java.lang.String-boolean-boolean-int-) | Inserts a checkbox form field at the current position. |
| [insertCheckBox(String name, boolean checkedValue, int size)](#insertCheckBox-java.lang.String-boolean-int-) | Inserts a checkbox form field at the current position. |
| [insertComboBox(String name, String[] items, int selectedIndex)](#insertComboBox-java.lang.String-java.lang.String---int-) | Inserts a combobox form field at the current position. |
| [insertDocument(Document srcDoc, int importFormatMode)](#insertDocument-com.aspose.words.Document-int-) |  |
| [insertDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#insertDocument-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions-) |  |
| [insertField(int fieldType, boolean updateField)](#insertField-int-boolean-) |  |
| [insertField(String fieldCode)](#insertField-java.lang.String-) | Inserts a Word field into a document. |
| [insertField(String fieldCode, String fieldValue)](#insertField-java.lang.String-java.lang.String-) | Inserts a Word field into a document without updating the field result. |
| [insertFootnote(int footnoteType, String footnoteText)](#insertFootnote-int-java.lang.String-) |  |
| [insertFootnote(int footnoteType, String footnoteText, String referenceMark)](#insertFootnote-int-java.lang.String-java.lang.String-) |  |
| [insertHorizontalRule()](#insertHorizontalRule--) | Inserts a horizontal rule shape into the document. |
| [insertHtml(String html)](#insertHtml-java.lang.String-) | Inserts an HTML string into the document. |
| [insertHtml(String html, boolean useBuilderFormatting)](#insertHtml-java.lang.String-boolean-) | Inserts an HTML string into the document. |
| [insertHtml(String html, int options)](#insertHtml-java.lang.String-int-) |  |
| [insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark)](#insertHyperlink-java.lang.String-java.lang.String-boolean-) | Inserts a hyperlink into the document. |
| [insertImage(byte[] imageBytes)](#insertImage-byte---) | Inserts an image from a byte array into the document. |
| [insertImage(byte[] imageBytes, double width, double height)](#insertImage-byte---double-double-) | Inserts an inline image from a byte array into the document and scales it to the specified size. |
| [insertImage(byte[] imageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-byte---int-double-int-double-double-double-int-) |  |
| [insertImage(BufferedImage image)](#insertImage-java.awt.image.BufferedImage-) | Inserts an image into the document. |
| [insertImage(BufferedImage image, double width, double height)](#insertImage-java.awt.image.BufferedImage-double-double-) | Inserts an inline image from a  object into the document and scales it to the specified size. |
| [insertImage(BufferedImage image, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.awt.image.BufferedImage-int-double-int-double-double-double-int-) |  |
| [insertImage(InputStream stream)](#insertImage-java.io.InputStream-) |  |
| [insertImage(InputStream stream, double width, double height)](#insertImage-java.io.InputStream-double-double-) |  |
| [insertImage(InputStream stream, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.io.InputStream-int-double-int-double-double-double-int-) |  |
| [insertImage(String fileName)](#insertImage-java.lang.String-) | Inserts an image from a file or URL into the document. |
| [insertImage(String fileName, double width, double height)](#insertImage-java.lang.String-double-double-) | Inserts an inline image from a file or URL into the document and scales it to the specified size. |
| [insertImage(String fileName, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.lang.String-int-double-int-double-double-double-int-) |  |
| [insertNode(Node node)](#insertNode-com.aspose.words.Node-) | Inserts a node before the cursor. |
| [insertOleObject(InputStream stream, String progId, boolean asIcon, InputStream presentation)](#insertOleObject-java.io.InputStream-java.lang.String-boolean-java.io.InputStream-) |  |
| [insertOleObject(String fileName, boolean isLinked, boolean asIcon, InputStream presentation)](#insertOleObject-java.lang.String-boolean-boolean-java.io.InputStream-) |  |
| [insertOleObject(String fileName, String progId, boolean isLinked, boolean asIcon, InputStream presentation)](#insertOleObject-java.lang.String-java.lang.String-boolean-boolean-java.io.InputStream-) |  |
| [insertOleObjectAsIcon(InputStream stream, String progId, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.io.InputStream-java.lang.String-java.lang.String-java.lang.String-) |  |
| [insertOleObjectAsIcon(String fileName, boolean isLinked, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.lang.String-boolean-java.lang.String-java.lang.String-) | Inserts an embedded or linked OLE object as icon into the document. |
| [insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.lang.String-java.lang.String-boolean-java.lang.String-java.lang.String-) | Inserts an embedded or linked OLE object as icon into the document. |
| [insertOnlineVideo(String videoUrl, double width, double height)](#insertOnlineVideo-java.lang.String-double-double-) | Inserts an online video object into the document and scales it to the specified size. |
| [insertOnlineVideo(String videoUrl, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertOnlineVideo-java.lang.String-int-double-int-double-double-double-int-) |  |
| [insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height)](#insertOnlineVideo-java.lang.String-java.lang.String-byte---double-double-) | Inserts an online video object into the document and scales it to the specified size. |
| [insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertOnlineVideo-java.lang.String-java.lang.String-byte---int-double-int-double-double-double-int-) |  |
| [insertParagraph()](#insertParagraph--) | Inserts a paragraph break into the document. |
| [insertShape(int shapeType, double width, double height)](#insertShape-int-double-double-) |  |
| [insertShape(int shapeType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertShape-int-int-double-int-double-double-double-int-) |  |
| [insertSignatureLine(SignatureLineOptions signatureLineOptions)](#insertSignatureLine-com.aspose.words.SignatureLineOptions-) | Inserts a signature line at the current position. |
| [insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType)](#insertSignatureLine-com.aspose.words.SignatureLineOptions-int-double-int-double-int-) |  |
| [insertStyleSeparator()](#insertStyleSeparator--) | Inserts style separator into the document. |
| [insertTableOfContents(String switches)](#insertTableOfContents-java.lang.String-) | Inserts a TOC (table of contents) field into the document. |
| [insertTextInput(String name, int type, String format, String fieldValue, int maxLength)](#insertTextInput-java.lang.String-int-java.lang.String-java.lang.String-int-) |  |
| [isAtEndOfParagraph()](#isAtEndOfParagraph--) | Returns true if the cursor is at the end of the current paragraph. |
| [isAtEndOfStructuredDocumentTag()](#isAtEndOfStructuredDocumentTag--) | Returns **true** if the cursor is at the end of a structured document tag. |
| [isAtStartOfParagraph()](#isAtStartOfParagraph--) | Returns true if the cursor is at the beginning of the current paragraph (no text before the cursor). |
| [moveTo(Node node)](#moveTo-com.aspose.words.Node-) | Moves the cursor to an inline node or to the end of a paragraph. |
| [moveToBookmark(String bookmarkName)](#moveToBookmark-java.lang.String-) | Moves the cursor to a bookmark. |
| [moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter)](#moveToBookmark-java.lang.String-boolean-boolean-) | Moves the cursor to a bookmark with greater precision. |
| [moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)](#moveToCell-int-int-int-int-) | Moves the cursor to a table cell in the current section. |
| [moveToDocumentEnd()](#moveToDocumentEnd--) | Moves the cursor to the end of the document. |
| [moveToDocumentStart()](#moveToDocumentStart--) | Moves the cursor to the beginning of the document. |
| [moveToField(Field field, boolean isAfter)](#moveToField-com.aspose.words.Field-boolean-) | Moves the cursor to a field in the document. |
| [moveToHeaderFooter(int headerFooterType)](#moveToHeaderFooter-int-) |  |
| [moveToMergeField(String fieldName)](#moveToMergeField-java.lang.String-) | Moves the cursor to the specified merge field. |
| [moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField)](#moveToMergeField-java.lang.String-boolean-boolean-) | Moves the merge field to the specified merge field. |
| [moveToParagraph(int paragraphIndex, int characterIndex)](#moveToParagraph-int-int-) | Moves the cursor to a paragraph in the current section. |
| [moveToSection(int sectionIndex)](#moveToSection-int-) | Moves the cursor to the beginning of the body in a specified section. |
| [moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex)](#moveToStructuredDocumentTag-com.aspose.words.StructuredDocumentTag-int-) | Moves the cursor to the structured document tag. |
| [moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)](#moveToStructuredDocumentTag-int-int-) | Moves the cursor to a structured document tag in the current section. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [popFont()](#popFont--) | Retrieves character formatting previously saved on the stack. |
| [pushFont()](#pushFont--) | Saves current character formatting onto the stack. |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [resetToDefaultAttrs()](#resetToDefaultAttrs--) |  |
| [setBold(boolean value)](#setBold-boolean-) | True if the font is formatted as bold. |
| [setCellAttr(int key, Object value)](#setCellAttr-int-java.lang.Object-) |  |
| [setDocument(Document value)](#setDocument-com.aspose.words.Document-) | Sets the [getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-) object that this object is attached to. |
| [setItalic(boolean value)](#setItalic-boolean-) | True if the font is formatted as italic. |
| [setRowAttr(int key, Object value)](#setRowAttr-int-java.lang.Object-) |  |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [setUnderline(int value)](#setUnderline-int-) | Gets/sets underline type for the current font. |
| [startBookmark(String bookmarkName)](#startBookmark-java.lang.String-) | Marks the current position in the document as a bookmark start. |
| [startColumnBookmark(String bookmarkName)](#startColumnBookmark-java.lang.String-) | Marks the current position in the document as a column bookmark start. |
| [startEditableRange()](#startEditableRange--) | Marks the current position in the document as an editable range start. |
| [startTable()](#startTable--) | Starts a table in the document. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
| [write(String text)](#write-java.lang.String-) | Inserts a string into the document at the current insert position. |
| [writeln()](#writeln--) | Inserts a paragraph break into the document. |
| [writeln(String text)](#writeln-java.lang.String-) | Inserts a string and a paragraph break into the document. |
### DocumentBuilder() {#DocumentBuilder--}
```
public DocumentBuilder()
```


Initializes a new instance of this class. Creates a new **DocumentBuilder** object and attaches it to a new [getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-) object.

### DocumentBuilder(Document doc) {#DocumentBuilder-com.aspose.words.Document-}
```
public DocumentBuilder(Document doc)
```


Initializes a new instance of this class. Creates a new **DocumentBuilder** object, attaches to the specified [getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-) object. The cursor is positioned at the beginning of the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document) | The Document object to attach to. |

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


Deletes a row from a table.

If the cursor is inside the row that is being deleted, the cursor is moved out to the next row or to the next paragraph after the table.

If you delete a row from a table that contains only one row, the whole table is deleted.

For the index parameters, when index is greater than or equal to 0, it specifies an index from the beginning with 0 being the first element. When index is less than 0, it specified an index from the end with -1 being the last element.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tableIndex | int | The index of the table. |
| rowIndex | int | The index of the row in the table. |

**Returns:**
[Row](../../com.aspose.words/row) - The row node that was just removed.
### endBookmark(String bookmarkName) {#endBookmark-java.lang.String-}
```
public BookmarkEnd endBookmark(String bookmarkName)
```


Marks the current position in the document as a bookmark end.

Bookmarks in a document can overlap and span any range. To create a valid bookmark you need to call both [startBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#startBookmark-java.lang.String-) and [endBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#endBookmark-java.lang.String-) with the same **bookmarkName** parameter.

Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | Name of the bookmark. |

**Returns:**
[BookmarkEnd](../../com.aspose.words/bookmarkend) - The bookmark end node that was just created.
### endColumnBookmark(String bookmarkName) {#endColumnBookmark-java.lang.String-}
```
public BookmarkEnd endColumnBookmark(String bookmarkName)
```


Marks the current position in the document as a column bookmark end. The position must be in a table cell.

A column bookmark covers one or more columns in a range of rows. To create a valid bookmark you need to call both [startColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#startColumnBookmark-java.lang.String-) and [endColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#endColumnBookmark-java.lang.String-) with the same **bookmarkName** parameter.

Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.

The actual position of the inserted [BookmarkEnd](../../com.aspose.words/bookmarkend) node may differ from the current document builder position.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | Name of the bookmark. |

**Returns:**
[BookmarkEnd](../../com.aspose.words/bookmarkend) - The bookmark end node that was just created.
### endEditableRange() {#endEditableRange--}
```
public EditableRangeEnd endEditableRange()
```


Marks the current position in the document as an editable range end.

Editable range in a document can overlap and span any range. To create a valid editable range you need to call both [startEditableRange()](../../com.aspose.words/documentbuilder\#startEditableRange--) and [endEditableRange()](../../com.aspose.words/documentbuilder\#endEditableRange--) or [endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder\#endEditableRange-com.aspose.words.EditableRangeStart-) methods.

Badly formed editable range will be ignored when the document is saved.

**Returns:**
[EditableRangeEnd](../../com.aspose.words/editablerangeend) - The editable range end node that was just created.
### endEditableRange(EditableRangeStart start) {#endEditableRange-com.aspose.words.EditableRangeStart-}
```
public EditableRangeEnd endEditableRange(EditableRangeStart start)
```


Marks the current position in the document as an editable range end.

Use this overload during creating nested editable ranges.

Editable range in a document can overlap and span any range. To create a valid editable range you need to call both [startEditableRange()](../../com.aspose.words/documentbuilder\#startEditableRange--) and [endEditableRange()](../../com.aspose.words/documentbuilder\#endEditableRange--) or [endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder\#endEditableRange-com.aspose.words.EditableRangeStart-) methods.

Badly formed editable range will be ignored when the document is saved.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| start | [EditableRangeStart](../../com.aspose.words/editablerangestart) | This editable range start. |

**Returns:**
[EditableRangeEnd](../../com.aspose.words/editablerangeend) - The editable range end node that was just created.
### endRow() {#endRow--}
```
public Row endRow()
```


Ends a table row in the document.

Call **EndRow** to end a table row. If you call [insertCell()](../../com.aspose.words/documentbuilder\#insertCell--) immediately after that, then the table continues on a new row.

Use the [getRowFormat()](../../com.aspose.words/documentbuilder\#getRowFormat--) property to specify row formatting.

**Returns:**
[Row](../../com.aspose.words/row) - The row node that was just finished.
### endTable() {#endTable--}
```
public Table endTable()
```


Ends a table in the document.

This method should be called only once after [endRow()](../../com.aspose.words/documentbuilder\#endRow--) was called. When called, **EndTable** moves the cursor out of the current cell to point just after the table.

**Returns:**
[Table](../../com.aspose.words/table) - The table node that was just finished.
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### fetchCellAttr(int key) {#fetchCellAttr-int-}
```
public Object fetchCellAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedCellAttr(int key) {#fetchInheritedCellAttr-int-}
```
public Object fetchInheritedCellAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRowAttr(int key) {#fetchInheritedRowAttr-int-}
```
public Object fetchInheritedRowAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRunAttr(int fontAttr) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int fontAttr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### fetchRowAttr(int key) {#fetchRowAttr-int-}
```
public Object fetchRowAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getBold() {#getBold--}
```
public boolean getBold()
```


True if the font is formatted as bold.

**Returns:**
boolean - The corresponding  boolean  value.
### getCellFormat() {#getCellFormat--}
```
public CellFormat getCellFormat()
```


Returns an object that represents current table cell formatting properties.

**Returns:**
[CellFormat](../../com.aspose.words/cellformat) - An object that represents current table cell formatting properties.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCurrentNode() {#getCurrentNode--}
```
public Node getCurrentNode()
```


Gets the node that is currently selected in this DocumentBuilder.

**CurrentNode** is a cursor of **DocumentBuilder** and points to a **Node** that is a direct child of a **Paragraph**. Any insert operations you perform using **DocumentBuilder** will insert before the **CurrentNode**.

When the current paragraph is empty or the cursor is positioned just before the end of a paragraph or structured document tag, **CurrentNode** returns null.

**Returns:**
[Node](../../com.aspose.words/node) - The node that is currently selected in this DocumentBuilder.
### getCurrentParagraph() {#getCurrentParagraph--}
```
public Paragraph getCurrentParagraph()
```


Gets the paragraph that is currently selected in this DocumentBuilder. [getCurrentNode()](../../com.aspose.words/documentbuilder\#getCurrentNode--)

**Returns:**
[Paragraph](../../com.aspose.words/paragraph) - The paragraph that is currently selected in this DocumentBuilder.
### getCurrentSection() {#getCurrentSection--}
```
public Section getCurrentSection()
```


Gets the section that is currently selected in this DocumentBuilder.

**Returns:**
[Section](../../com.aspose.words/section) - The section that is currently selected in this DocumentBuilder.
### getCurrentStory() {#getCurrentStory--}
```
public Story getCurrentStory()
```


Gets the story that is currently selected in this DocumentBuilder.

**Returns:**
[Story](../../com.aspose.words/story) - The story that is currently selected in this DocumentBuilder.
### getCurrentStructuredDocumentTag() {#getCurrentStructuredDocumentTag--}
```
public StructuredDocumentTag getCurrentStructuredDocumentTag()
```


Gets the structured document tag that is currently selected in this DocumentBuilder.

**Returns:**
[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) - The structured document tag that is currently selected in this DocumentBuilder.
### getDirectCellAttr(int key) {#getDirectCellAttr-int-}
```
public Object getDirectCellAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRowAttr(int key) {#getDirectRowAttr-int-}
```
public Object getDirectRowAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int fontAttr) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int fontAttr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### getDocument() {#getDocument--}
```
public Document getDocument()
```


Gets the [getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-) object that this object is attached to.

**Returns:**
[Document](../../com.aspose.words/document) - The [getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-) object that this object is attached to.
### getFont() {#getFont--}
```
public Font getFont()
```


Returns an object that represents current font formatting properties.

Use **Font** to access and modify font formatting properties.

Specify font formatting before inserting text.

**Returns:**
[Font](../../com.aspose.words/font) - An object that represents current font formatting properties.
### getItalic() {#getItalic--}
```
public boolean getItalic()
```


True if the font is formatted as italic.

**Returns:**
boolean - The corresponding  boolean  value.
### getListFormat() {#getListFormat--}
```
public ListFormat getListFormat()
```


Returns an object that represents current list formatting properties.

**Returns:**
[ListFormat](../../com.aspose.words/listformat) - An object that represents current list formatting properties.
### getPageSetup() {#getPageSetup--}
```
public PageSetup getPageSetup()
```


Returns an object that represents current page setup and section properties.

**Returns:**
[PageSetup](../../com.aspose.words/pagesetup) - An object that represents current page setup and section properties.
### getParagraphFormat() {#getParagraphFormat--}
```
public ParagraphFormat getParagraphFormat()
```


Returns an object that represents current paragraph formatting properties.

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat) - An object that represents current paragraph formatting properties.
### getRowFormat() {#getRowFormat--}
```
public RowFormat getRowFormat()
```


Returns an object that represents current table row formatting properties.

**Returns:**
[RowFormat](../../com.aspose.words/rowformat) - An object that represents current table row formatting properties.
### getUnderline() {#getUnderline--}
```
public int getUnderline()
```


Gets/sets underline type for the current font.

**Returns:**
int - The corresponding  int  value. The returned value is one of [Underline](../../com.aspose.words/underline) constants.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### insertBreak(int breakType) {#insertBreak-int-}
```
public void insertBreak(int breakType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| breakType | int |  |

### insertCell() {#insertCell--}
```
public Cell insertCell()
```


Inserts a table cell into the document.

To start a table, just call **InsertCell**. After this, any content you add using other methods of the [DocumentBuilder](../../com.aspose.words/documentbuilder) class will be added to the current cell.

To start a new cell in the same row, call **InsertCell** again.

To end a table row call [endRow()](../../com.aspose.words/documentbuilder\#endRow--).

Use the [getCellFormat()](../../com.aspose.words/documentbuilder\#getCellFormat--) property to specify cell formatting.

**Returns:**
[Cell](../../com.aspose.words/cell) - The cell node that was just inserted.
### insertChart(int chartType, double width, double height) {#insertChart-int-double-double-}
```
public Shape insertChart(int chartType, double width, double height)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| chartType | int |  |
| width | double |  |
| height | double |  |

**Returns:**
[Shape](../../com.aspose.words/shape)
### insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertChart-int-int-double-int-double-double-double-int-}
```
public Shape insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| chartType | int |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| width | double |  |
| height | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape)
### insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size) {#insertCheckBox-java.lang.String-boolean-boolean-int-}
```
public FormField insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size)
```


Inserts a checkbox form field at the current position.

If you specify a name for the form field, then a bookmark is automatically created with the same name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the form field. Can be an empty string. The value longer than 20 characters will be truncated. |
| defaultValue | boolean | Default value of the checkbox form field. |
| checkedValue | boolean | Current checked status of the checkbox form field. |
| size | int | Specifies the size of the checkbox in points. Specify 0 for MS Word to calculate the size of the checkbox automatically. |

**Returns:**
[FormField](../../com.aspose.words/formfield) - The form field node that was just inserted.
### insertCheckBox(String name, boolean checkedValue, int size) {#insertCheckBox-java.lang.String-boolean-int-}
```
public FormField insertCheckBox(String name, boolean checkedValue, int size)
```


Inserts a checkbox form field at the current position.

If you specify a name for the form field, then a bookmark is automatically created with the same name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the form field. Can be an empty string. The value longer than 20 characters will be truncated. |
| checkedValue | boolean | Checked status of the checkbox form field. |
| size | int | Specifies the size of the checkbox in points. Specify 0 for MS Word to calculate the size of the checkbox automatically. |

**Returns:**
[FormField](../../com.aspose.words/formfield) - The form field node that was just inserted.
### insertComboBox(String name, String[] items, int selectedIndex) {#insertComboBox-java.lang.String-java.lang.String---int-}
```
public FormField insertComboBox(String name, String[] items, int selectedIndex)
```


Inserts a combobox form field at the current position.

If you specify a name for the form field, then a bookmark is automatically created with the same name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the form field. Can be an empty string. The value longer than 20 characters will be truncated. |
| items | java.lang.String[] | The items of the ComboBox. Maximum is 25 items. |
| selectedIndex | int | The index of the selected item in the ComboBox. |

**Returns:**
[FormField](../../com.aspose.words/formfield) - The form field node that was just inserted.
### insertDocument(Document srcDoc, int importFormatMode) {#insertDocument-com.aspose.words.Document-int-}
```
public Node insertDocument(Document srcDoc, int importFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document) |  |
| importFormatMode | int |  |

**Returns:**
[Node](../../com.aspose.words/node)
### insertDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#insertDocument-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions-}
```
public Node insertDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions) |  |

**Returns:**
[Node](../../com.aspose.words/node)
### insertField(int fieldType, boolean updateField) {#insertField-int-boolean-}
```
public Field insertField(int fieldType, boolean updateField)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldType | int |  |
| updateField | boolean |  |

**Returns:**
[Field](../../com.aspose.words/field)
### insertField(String fieldCode) {#insertField-java.lang.String-}
```
public Field insertField(String fieldCode)
```


Inserts a Word field into a document.  Inserts a Word field into a document and updates the field result.

This method inserts a field into a document and updates the field result immediately. Aspose.Words can update fields of most types, but not all. For more details see the [insertField(java.lang.String, java.lang.String)](../../com.aspose.words/documentbuilder\#insertField-java.lang.String--java.lang.String-) overload.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | java.lang.String | The field code to insert (without curly braces). |

**Returns:**
[Field](../../com.aspose.words/field) - A [Field](../../com.aspose.words/field) object that represents the inserted field.
### insertField(String fieldCode, String fieldValue) {#insertField-java.lang.String-java.lang.String-}
```
public Field insertField(String fieldCode, String fieldValue)
```


Inserts a Word field into a document without updating the field result.

Fields in Microsoft Word documents consist of a field code and a field result. The field code is like a formula and the field result is like the value that the formula produces. The field code may also contain field switches that are like additional instructions to perform a specific action.

You can switch between displaying field codes and results in your document in Microsoft Word using the keyboard shortcut Alt+F9. Field codes appear between curly braces ( \{ \} ).

To create a field, you need to specify a field type, field code and a "placeholder" field value. If you are not sure about a particular field code syntax, create the field in Microsoft Word first and switch to see its field code.

Aspose.Words can calculate field results for most of the field types, but this method does not update the field result automatically. Because the field result is not calculated automatically, you are expected to pass some string value (or even an empty string) that will be inserted into the field result. This value will remain in the field result as a placeholder until the field is updated. To update the field result you can call [Field.update()](../../com.aspose.words/field\#update--) on the field object returned to you or [Document.updateFields()](../../com.aspose.words/document\#updateFields--) to update fields in the whole document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | java.lang.String | The field code to insert (without curly braces). |
| fieldValue | java.lang.String | The field value to insert. Pass null for fields that do not have a value. |

**Returns:**
[Field](../../com.aspose.words/field) - A [Field](../../com.aspose.words/field) object that represents the inserted field.
### insertFootnote(int footnoteType, String footnoteText) {#insertFootnote-int-java.lang.String-}
```
public Footnote insertFootnote(int footnoteType, String footnoteText)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| footnoteType | int |  |
| footnoteText | java.lang.String |  |

**Returns:**
[Footnote](../../com.aspose.words/footnote)
### insertFootnote(int footnoteType, String footnoteText, String referenceMark) {#insertFootnote-int-java.lang.String-java.lang.String-}
```
public Footnote insertFootnote(int footnoteType, String footnoteText, String referenceMark)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| footnoteType | int |  |
| footnoteText | java.lang.String |  |
| referenceMark | java.lang.String |  |

**Returns:**
[Footnote](../../com.aspose.words/footnote)
### insertHorizontalRule() {#insertHorizontalRule--}
```
public Shape insertHorizontalRule()
```


Inserts a horizontal rule shape into the document.

**Returns:**
[Shape](../../com.aspose.words/shape) - The shape that is a horizontal rule.
### insertHtml(String html) {#insertHtml-java.lang.String-}
```
public void insertHtml(String html)
```


Inserts an HTML string into the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| html | java.lang.String | An HTML string to insert into the document. You can use this method to insert an HTML fragment or whole HTML document. |

### insertHtml(String html, boolean useBuilderFormatting) {#insertHtml-java.lang.String-boolean-}
```
public void insertHtml(String html, boolean useBuilderFormatting)
```


Inserts an HTML string into the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| html | java.lang.String | An HTML string to insert into the document. |
| useBuilderFormatting | boolean | A value indicating whether formatting specified in [DocumentBuilder](../../com.aspose.words/documentbuilder) is used as base formatting for text imported from HTML.

You can use this method to insert an HTML fragment or whole HTML document.

When  useBuilderFormatting  is  false , [DocumentBuilder](../../com.aspose.words/documentbuilder) formating is ignored and formatting of inserted text is based on default HTML formatting. As a result, the text looks as it is rendered in browsers.

When  useBuilderFormatting  is  true , formatting of inserted text is based on [DocumentBuilder](../../com.aspose.words/documentbuilder) formatting, and the text looks as if it were inserted with [write(java.lang.String)](../../com.aspose.words/documentbuilder\#write-java.lang.String-). |

### insertHtml(String html, int options) {#insertHtml-java.lang.String-int-}
```
public void insertHtml(String html, int options)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| html | java.lang.String |  |
| options | int |  |

### insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark) {#insertHyperlink-java.lang.String-java.lang.String-boolean-}
```
public Field insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark)
```


Inserts a hyperlink into the document.

Note that you need to specify font formatting for the hyperlink display text explicitly using the [getFont()](../../com.aspose.words/documentbuilder\#getFont--) property.

This methods internally calls [insertField(java.lang.String)](../../com.aspose.words/documentbuilder\#insertField-java.lang.String-) to insert an MS Word HYPERLINK field into the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| displayText | java.lang.String | Text of the link to be displayed in the document. |
| urlOrBookmark | java.lang.String | Link destination. Can be a url or a name of a bookmark inside the document. This method always adds apostrophes at the beginning and end of the url. |
| isBookmark | boolean | True if the previous parameter is a name of a bookmark inside the document; false is the previous parameter is a URL. |

**Returns:**
[Field](../../com.aspose.words/field) - A [Field](../../com.aspose.words/field) object that represents the inserted field.
### insertImage(byte[] imageBytes) {#insertImage-byte---}
```
public Shape insertImage(byte[] imageBytes)
```


Inserts an image from a byte array into the document. The image is inserted inline and at 100% scale.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | byte[] | The byte array that contains the image. |

**Returns:**
[Shape](../../com.aspose.words/shape) - The image node that was just inserted.

You can change the image size, location, positioning method and other settings using the [Shape](../../com.aspose.words/shape) object returned by this method.
### insertImage(byte[] imageBytes, double width, double height) {#insertImage-byte---double-double-}
```
public Shape insertImage(byte[] imageBytes, double width, double height)
```


Inserts an inline image from a byte array into the document and scales it to the specified size.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | byte[] | The byte array that contains the image. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

**Returns:**
[Shape](../../com.aspose.words/shape) - The image node that was just inserted.

You can change the image size, location, positioning method and other settings using the [Shape](../../com.aspose.words/shape) object returned by this method.
### insertImage(byte[] imageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-byte---int-double-int-double-double-double-int-}
```
public Shape insertImage(byte[] imageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | byte[] |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| width | double |  |
| height | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape)
### insertImage(BufferedImage image) {#insertImage-java.awt.image.BufferedImage-}
```
public Shape insertImage(BufferedImage image)
```


Inserts an image into the document.  Inserts an image from a  object into the document. The image is inserted inline and at 100% scale.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | The image to insert into the document. |

**Returns:**
[Shape](../../com.aspose.words/shape) - The image node that was just inserted.

You can change the image size, location, positioning method and other settings using the [Shape](../../com.aspose.words/shape) object returned by this method.

Aspose.Words will insert the image in the PNG format and with default settings. If you want to insert a  BufferedImage  in another format or with other settings, you need to save the image into a byte array and use [insertImage(byte[])](../../com.aspose.words/documentbuilder\#insertImage-byte---).
### insertImage(BufferedImage image, double width, double height) {#insertImage-java.awt.image.BufferedImage-double-double-}
```
public Shape insertImage(BufferedImage image, double width, double height)
```


Inserts an inline image from a  object into the document and scales it to the specified size.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | The image to insert into the document. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

**Returns:**
[Shape](../../com.aspose.words/shape) - The image node that was just inserted.

You can change the image size, location, positioning method and other settings using the [Shape](../../com.aspose.words/shape) object returned by this method.

Aspose.Words will insert the image in the PNG format and with default settings. If you want to insert a  BufferedImage  in another format or with other settings, you need to save the image into a byte array and use [insertImage(byte[])](../../com.aspose.words/documentbuilder\#insertImage-byte---).
### insertImage(BufferedImage image, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.awt.image.BufferedImage-int-double-int-double-double-double-int-}
```
public Shape insertImage(BufferedImage image, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| image | java.awt.image.BufferedImage |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| width | double |  |
| height | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape)
### insertImage(InputStream stream) {#insertImage-java.io.InputStream-}
```
public Shape insertImage(InputStream stream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |

**Returns:**
[Shape](../../com.aspose.words/shape)
### insertImage(InputStream stream, double width, double height) {#insertImage-java.io.InputStream-double-double-}
```
public Shape insertImage(InputStream stream, double width, double height)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| width | double |  |
| height | double |  |

**Returns:**
[Shape](../../com.aspose.words/shape)
### insertImage(InputStream stream, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.io.InputStream-int-double-int-double-double-double-int-}
```
public Shape insertImage(InputStream stream, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| width | double |  |
| height | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape)
### insertImage(String fileName) {#insertImage-java.lang.String-}
```
public Shape insertImage(String fileName)
```


Inserts an image from a file or URL into the document. The image is inserted inline and at 100% scale.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The file with the image. Can be any valid local or remote URI. |

**Returns:**
[Shape](../../com.aspose.words/shape) - The image node that was just inserted.

This overload will automatically download the image before inserting into the document if you specify a remote URI.

You can change the image size, location, positioning method and other settings using the [Shape](../../com.aspose.words/shape) object returned by this method.
### insertImage(String fileName, double width, double height) {#insertImage-java.lang.String-double-double-}
```
public Shape insertImage(String fileName, double width, double height)
```


Inserts an inline image from a file or URL into the document and scales it to the specified size.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The file that contains the image. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

**Returns:**
[Shape](../../com.aspose.words/shape) - The image node that was just inserted.

You can change the image size, location, positioning method and other settings using the [Shape](../../com.aspose.words/shape) object returned by this method.
### insertImage(String fileName, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.lang.String-int-double-int-double-double-double-int-}
```
public Shape insertImage(String fileName, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| width | double |  |
| height | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape)
### insertNode(Node node) {#insertNode-com.aspose.words.Node-}
```
public void insertNode(Node node)
```


Inserts a node before the cursor.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) |  |

### insertOleObject(InputStream stream, String progId, boolean asIcon, InputStream presentation) {#insertOleObject-java.io.InputStream-java.lang.String-boolean-java.io.InputStream-}
```
public Shape insertOleObject(InputStream stream, String progId, boolean asIcon, InputStream presentation)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| progId | java.lang.String |  |
| asIcon | boolean |  |
| presentation | java.io.InputStream |  |

**Returns:**
[Shape](../../com.aspose.words/shape)
### insertOleObject(String fileName, boolean isLinked, boolean asIcon, InputStream presentation) {#insertOleObject-java.lang.String-boolean-boolean-java.io.InputStream-}
```
public Shape insertOleObject(String fileName, boolean isLinked, boolean asIcon, InputStream presentation)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String |  |
| isLinked | boolean |  |
| asIcon | boolean |  |
| presentation | java.io.InputStream |  |

**Returns:**
[Shape](../../com.aspose.words/shape)
### insertOleObject(String fileName, String progId, boolean isLinked, boolean asIcon, InputStream presentation) {#insertOleObject-java.lang.String-java.lang.String-boolean-boolean-java.io.InputStream-}
```
public Shape insertOleObject(String fileName, String progId, boolean isLinked, boolean asIcon, InputStream presentation)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String |  |
| progId | java.lang.String |  |
| isLinked | boolean |  |
| asIcon | boolean |  |
| presentation | java.io.InputStream |  |

**Returns:**
[Shape](../../com.aspose.words/shape)
### insertOleObjectAsIcon(InputStream stream, String progId, String iconFile, String iconCaption) {#insertOleObjectAsIcon-java.io.InputStream-java.lang.String-java.lang.String-java.lang.String-}
```
public Shape insertOleObjectAsIcon(InputStream stream, String progId, String iconFile, String iconCaption)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| progId | java.lang.String |  |
| iconFile | java.lang.String |  |
| iconCaption | java.lang.String |  |

**Returns:**
[Shape](../../com.aspose.words/shape)
### insertOleObjectAsIcon(String fileName, boolean isLinked, String iconFile, String iconCaption) {#insertOleObjectAsIcon-java.lang.String-boolean-java.lang.String-java.lang.String-}
```
public Shape insertOleObjectAsIcon(String fileName, boolean isLinked, String iconFile, String iconCaption)
```


Inserts an embedded or linked OLE object as icon into the document. Allows to specify icon file and caption. Detects OLE object type using file extension.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Full path to the file. |
| isLinked | boolean | If true then linked OLE object is inserted otherwise embedded OLE object is inserted. |
| iconFile | java.lang.String | Full path to the ICO file. If the value is null, Aspose.Words will use a predefined image. |
| iconCaption | java.lang.String | Icon caption. If the value is null, Aspose.Words will use the file name. |

**Returns:**
[Shape](../../com.aspose.words/shape) - Shape node containing Ole object and inserted at the current Builder position.
### insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption) {#insertOleObjectAsIcon-java.lang.String-java.lang.String-boolean-java.lang.String-java.lang.String-}
```
public Shape insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption)
```


Inserts an embedded or linked OLE object as icon into the document. Allows to specify icon file and caption. Detects OLE object type using given progID parameter.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Full path to the file. |
| progId | java.lang.String | ProgId of OLE object. |
| isLinked | boolean | If true then linked OLE object is inserted otherwise embedded OLE object is inserted. |
| iconFile | java.lang.String | Full path to the ICO file. If the value is null, Aspose.Words will use a predefined image. |
| iconCaption | java.lang.String | Icon caption. If the value is null, Aspose.Words will use the file name. |

**Returns:**
[Shape](../../com.aspose.words/shape) - Shape node containing Ole object and inserted at the current Builder position.
### insertOnlineVideo(String videoUrl, double width, double height) {#insertOnlineVideo-java.lang.String-double-double-}
```
public Shape insertOnlineVideo(String videoUrl, double width, double height)
```


Inserts an online video object into the document and scales it to the specified size.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| videoUrl | java.lang.String | The URL to the video. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

**Returns:**
[Shape](../../com.aspose.words/shape) - The image node that was just inserted.

You can change the image size, location, positioning method and other settings using the [Shape](../../com.aspose.words/shape) object returned by this method.

Insertion of online video from the following resources is supported:

 *  https://www.youtube.com/
 *  https://vimeo.com/

If your online video is not displaying correctly, use [insertOnlineVideo(java.lang.String, java.lang.String, byte[], double, double)](../../com.aspose.words/documentbuilder\#insertOnlineVideo-java.lang.String--java.lang.String--byte----double--double-), which accepts custom embedded html code.

The code for embedding video can vary between providers, consult your corresponding provider of choice for details.
### insertOnlineVideo(String videoUrl, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertOnlineVideo-java.lang.String-int-double-int-double-double-double-int-}
```
public Shape insertOnlineVideo(String videoUrl, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| videoUrl | java.lang.String |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| width | double |  |
| height | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape)
### insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height) {#insertOnlineVideo-java.lang.String-java.lang.String-byte---double-double-}
```
public Shape insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height)
```


Inserts an online video object into the document and scales it to the specified size.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| videoUrl | java.lang.String | The URL to the video. |
| videoEmbedCode | java.lang.String | The embed code for the video. |
| thumbnailImageBytes | byte[] | The thumbnail image bytes. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

**Returns:**
[Shape](../../com.aspose.words/shape) - The image node that was just inserted.

You can change the image size, location, positioning method and other settings using the [Shape](../../com.aspose.words/shape) object returned by this method.
### insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertOnlineVideo-java.lang.String-java.lang.String-byte---int-double-int-double-double-double-int-}
```
public Shape insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parameter | Type | Description |
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

**Returns:**
[Shape](../../com.aspose.words/shape)
### insertParagraph() {#insertParagraph--}
```
public Paragraph insertParagraph()
```


Inserts a paragraph break into the document.

Current paragraph formatting specified by the [getParagraphFormat()](../../com.aspose.words/documentbuilder\#getParagraphFormat--) property is used.

Breaks the current paragraph in two. After inserting the paragraph, the cursor is placed at the beginning of the new paragraph.

**Returns:**
[Paragraph](../../com.aspose.words/paragraph) - The paragraph node that was just inserted. It is the same node as [getCurrentParagraph()](../../com.aspose.words/documentbuilder\#getCurrentParagraph--).
### insertShape(int shapeType, double width, double height) {#insertShape-int-double-double-}
```
public Shape insertShape(int shapeType, double width, double height)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| shapeType | int |  |
| width | double |  |
| height | double |  |

**Returns:**
[Shape](../../com.aspose.words/shape)
### insertShape(int shapeType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertShape-int-int-double-int-double-double-double-int-}
```
public Shape insertShape(int shapeType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| shapeType | int |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| width | double |  |
| height | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape)
### insertSignatureLine(SignatureLineOptions signatureLineOptions) {#insertSignatureLine-com.aspose.words.SignatureLineOptions-}
```
public Shape insertSignatureLine(SignatureLineOptions signatureLineOptions)
```


Inserts a signature line at the current position.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| signatureLineOptions | [SignatureLineOptions](../../com.aspose.words/signaturelineoptions) | The object that stores parameters of creating signature line. |

**Returns:**
[Shape](../../com.aspose.words/shape) - The signature line node that was just inserted.
### insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType) {#insertSignatureLine-com.aspose.words.SignatureLineOptions-int-double-int-double-int-}
```
public Shape insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| signatureLineOptions | [SignatureLineOptions](../../com.aspose.words/signaturelineoptions) |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape)
### insertStyleSeparator() {#insertStyleSeparator--}
```
public void insertStyleSeparator()
```


Inserts style separator into the document. This method allows to apply different paragraph styles to two different parts of a text line.

### insertTableOfContents(String switches) {#insertTableOfContents-java.lang.String-}
```
public Field insertTableOfContents(String switches)
```


Inserts a TOC (table of contents) field into the document.

This method inserts a TOC (table of contents) field into the document at the current position.

A table of contents in a Word document can be built in a number of ways and formatted using a variety of options. The way the table is built and displayed by Microsoft Word is controlled by the field switches.

The easiest way to specify the switches is to insert and configure a table of contents into a Word document using the Insert->Reference->Index and Tables menu, then switch display of field codes on to see the switches. You can press Alt+F9 in Microsoft Word to toggle display of field codes on or off.

For example, after creating a table of contents, the following field is inserted into the document: **\{ TOC \\o "1-3" \\h \\z \}**. You can copy **\\o "1-3" \\h \\z**  and use it as the switches parameter.

Note that **InsertTableOfContents** will only insert a TOC field, but will not actually build the table of contents. The table of contents is built by Microsoft Word when the field is updated.

If you insert a table of contents using this method and then open the file in Microsoft Word, you will not see the table of contents because the TOC field has not yet been updated.

In Microsoft Word, fields are not automatically updated when a document is opened, but you can update fields in a document at any time by pressing F9.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| switches | java.lang.String | The TOC field switches. |

**Returns:**
[Field](../../com.aspose.words/field)
### insertTextInput(String name, int type, String format, String fieldValue, int maxLength) {#insertTextInput-java.lang.String-int-java.lang.String-java.lang.String-int-}
```
public FormField insertTextInput(String name, int type, String format, String fieldValue, int maxLength)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String |  |
| type | int |  |
| format | java.lang.String |  |
| fieldValue | java.lang.String |  |
| maxLength | int |  |

**Returns:**
[FormField](../../com.aspose.words/formfield)
### isAtEndOfParagraph() {#isAtEndOfParagraph--}
```
public boolean isAtEndOfParagraph()
```


Returns true if the cursor is at the end of the current paragraph.

**Returns:**
boolean - True if the cursor is at the end of the current paragraph.
### isAtEndOfStructuredDocumentTag() {#isAtEndOfStructuredDocumentTag--}
```
public boolean isAtEndOfStructuredDocumentTag()
```


Returns **true** if the cursor is at the end of a structured document tag.

**Returns:**
boolean - **true** if the cursor is at the end of a structured document tag.
### isAtStartOfParagraph() {#isAtStartOfParagraph--}
```
public boolean isAtStartOfParagraph()
```


Returns true if the cursor is at the beginning of the current paragraph (no text before the cursor).

**Returns:**
boolean - True if the cursor is at the beginning of the current paragraph (no text before the cursor).
### moveTo(Node node) {#moveTo-com.aspose.words.Node-}
```
public void moveTo(Node node)
```


Moves the cursor to an inline node or to the end of a paragraph.

When *node* is an inline-level node, the cursor is moved to this node and further content will be inserted before that node.

When *node* is a **Paragraph**, the cursor is moved to the end of the paragraph and further content will be inserted just before the paragraph break.

When *node* is a block-level node but not a Paragraph, the cursor is moved to the end of the first paragraph into block-level node and further content will be inserted just before the paragraph break.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) | The node must be a paragraph or a direct child of a paragraph. |

### moveToBookmark(String bookmarkName) {#moveToBookmark-java.lang.String-}
```
public boolean moveToBookmark(String bookmarkName)
```


Moves the cursor to a bookmark.

Moves the cursor to a position just after the start of the bookmark with the specified name.

The comparison is not case-sensitive. If the bookmark was not found, false is returned and the cursor is not moved.

Inserting new text does not replace existing text of the bookmark.

Note that some bookmarks in the document are assigned to form fields. Moving to such a bookmark and inserting text there inserts the text into the form field code. Although this will not invalidate the form field, the inserted text will not be visible because it becomes part of the field code.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | The name of the bookmark to move the cursor to. |

**Returns:**
boolean - True if the bookmark was found; false otherwise.
### moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter) {#moveToBookmark-java.lang.String-boolean-boolean-}
```
public boolean moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter)
```


Moves the cursor to a bookmark with greater precision.

Moves the cursor to a position before or after the bookmark start or end.

If desired position is not at inline level, moves to the next paragraph.

The comparison is not case-sensitive. If the bookmark was not found, false is returned and the cursor is not moved.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | The name of the bookmark to move the cursor to. |
| isStart | boolean | When true, moves the cursor to the beginning of the bookmark. When false, moves the cursor to the end of the bookmark. |
| isAfter | boolean | When true, moves the cursor to be after the bookmark start or end position. When false, moves the cursor to be before the bookmark start or end position. |

**Returns:**
boolean - True if the bookmark was found; false otherwise.
### moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex) {#moveToCell-int-int-int-int-}
```
public void moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)
```


Moves the cursor to a table cell in the current section.

The navigation is performed inside the current story of the current section.

For the index parameters, when index is greater than or equal to 0, it specifies an index from the beginning with 0 being the first element. When index is less than 0, it specified an index from the end with -1 being the last element.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tableIndex | int | The index of the table to move to. |
| rowIndex | int | The index of the row in the table. |
| columnIndex | int | The index of the column in the table. |
| characterIndex | int | The index of the character inside the cell. A negative value allows you to specify a position from the end of the cell. Use -1 to move to the end of the cell. |

### moveToDocumentEnd() {#moveToDocumentEnd--}
```
public void moveToDocumentEnd()
```


Moves the cursor to the end of the document.

### moveToDocumentStart() {#moveToDocumentStart--}
```
public void moveToDocumentStart()
```


Moves the cursor to the beginning of the document.

### moveToField(Field field, boolean isAfter) {#moveToField-com.aspose.words.Field-boolean-}
```
public void moveToField(Field field, boolean isAfter)
```


Moves the cursor to a field in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| field | [Field](../../com.aspose.words/field) | The field to move the cursor to. |
| isAfter | boolean | When true, moves the cursor to be after the field end. When false, moves the cursor to be before the field start. |

### moveToHeaderFooter(int headerFooterType) {#moveToHeaderFooter-int-}
```
public void moveToHeaderFooter(int headerFooterType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| headerFooterType | int |  |

### moveToMergeField(String fieldName) {#moveToMergeField-java.lang.String-}
```
public boolean moveToMergeField(String fieldName)
```


Moves the cursor to the specified merge field.  Moves the cursor to a position just beyond the specified merge field and removes the merge field.

Note that this method deletes the merge field from the document after moving the cursor.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldName | java.lang.String | The case-insensitive name of the mail merge field. |

**Returns:**
boolean - True if the merge field was found and the cursor was moved; false otherwise.
### moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField) {#moveToMergeField-java.lang.String-boolean-boolean-}
```
public boolean moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField)
```


Moves the merge field to the specified merge field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldName | java.lang.String | The case-insensitive name of the mail merge field. |
| isAfter | boolean | When true, moves the cursor to be after the field end. When false, moves the cursor to be before the field start. |
| isDeleteField | boolean | When true, deletes the merge field. |

**Returns:**
boolean - True if the merge field was found and the cursor was moved; false otherwise.
### moveToParagraph(int paragraphIndex, int characterIndex) {#moveToParagraph-int-int-}
```
public void moveToParagraph(int paragraphIndex, int characterIndex)
```


Moves the cursor to a paragraph in the current section.

The navigation is performed inside the current story of the current section. That is, if you moved the cursor to the primary header of the first section, then paragraphIndex specified the index of the paragraph inside that header of that section.

When paragraphIndex is greater than or equal to 0, it specifies an index from the beginning of the section with 0 being the first paragraph. When paragraphIndex is less than 0, it specified an index from the end of the section with -1 being the last paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| paragraphIndex | int | The index of the paragraph to move to. |
| characterIndex | int | The index of the character inside the paragraph. A negative value allows you to specify a position from the end of the paragraph. Use -1 to move to the end of the paragraph. |

### moveToSection(int sectionIndex) {#moveToSection-int-}
```
public void moveToSection(int sectionIndex)
```


Moves the cursor to the beginning of the body in a specified section.

When sectionIndex is greater than or equal to 0, it specifies an index from the beginning of the document with 0 being the first section. When sectionIndex is less than 0, it specified an index from the end of the document with -1 being the last section.

The cursor is moved to the first paragraph in the **Body** of the specified section.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sectionIndex | int | The index of the section to move to. |

### moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex) {#moveToStructuredDocumentTag-com.aspose.words.StructuredDocumentTag-int-}
```
public void moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex)
```


Moves the cursor to the structured document tag.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| structuredDocumentTag | [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) | The structured document tag to move to. |
| characterIndex | int | The index of the character inside the structured document tag. A negative value allows you to specify a position from the end of the structured document tag. Use -1 to move to the end of the structured document tag. If the structured document tag is at the block level, and you want to move the cursor to the end of its last paragraph, specify -2. |

### moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex) {#moveToStructuredDocumentTag-int-int-}
```
public void moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```


Moves the cursor to a structured document tag in the current section.

The navigation is performed inside the current story of the current section. That is, if you moved the cursor to the primary header of the first section, then  structuredDocumentTagIndex  specified the index of the structured document tag inside that header of that section.

When  structuredDocumentTagIndex  is greater than or equal to 0, it specifies an index from the beginning of the section with 0 being the first structured document tag. When  structuredDocumentTagIndex  is less than 0, it specified an index from the end of the section with -1 being the last structured document tag.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| structuredDocumentTagIndex | int | The index of the structured document tag to move to. |
| characterIndex | int | The index of the character inside the structured document tag. A negative value allows you to specify a position from the end of the structured document tag. Use -1 to move to the end of the structured document tag. If the structured document tag is at the block level, and you want to move the cursor to the end of its last paragraph, specify -2. |

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


Retrieves character formatting previously saved on the stack.

### pushFont() {#pushFont--}
```
public void pushFont()
```


Saves current character formatting onto the stack.

### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
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


True if the font is formatted as bold.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setCellAttr(int key, Object value) {#setCellAttr-int-java.lang.Object-}
```
public void setCellAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setDocument(Document value) {#setDocument-com.aspose.words.Document-}
```
public void setDocument(Document value)
```


Sets the [getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-) object that this object is attached to.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [Document](../../com.aspose.words/document) | The [getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-) object that this object is attached to. |

### setItalic(boolean value) {#setItalic-boolean-}
```
public void setItalic(boolean value)
```


True if the font is formatted as italic.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setRowAttr(int key, Object value) {#setRowAttr-int-java.lang.Object-}
```
public void setRowAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setRunAttr(int fontAttr, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int fontAttr, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |
| value | java.lang.Object |  |

### setUnderline(int value) {#setUnderline-int-}
```
public void setUnderline(int value)
```


Gets/sets underline type for the current font.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [Underline](../../com.aspose.words/underline) constants. |

### startBookmark(String bookmarkName) {#startBookmark-java.lang.String-}
```
public BookmarkStart startBookmark(String bookmarkName)
```


Marks the current position in the document as a bookmark start.

Bookmarks in a document can overlap and span any range. To create a valid bookmark you need to call both [startBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#startBookmark-java.lang.String-) and [endBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#endBookmark-java.lang.String-) with the same **bookmarkName** parameter.

Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | Name of the bookmark. |

**Returns:**
[BookmarkStart](../../com.aspose.words/bookmarkstart) - The bookmark start node that was just created.
### startColumnBookmark(String bookmarkName) {#startColumnBookmark-java.lang.String-}
```
public BookmarkStart startColumnBookmark(String bookmarkName)
```


Marks the current position in the document as a column bookmark start. The position must be in a table cell.

A column bookmark covers one or more columns in a range of rows. To create a valid bookmark you need to call both [startColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#startColumnBookmark-java.lang.String-) and [endColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#endColumnBookmark-java.lang.String-) with the same **bookmarkName** parameter.

Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.

The actual position of the inserted [BookmarkStart](../../com.aspose.words/bookmarkstart) node may differ from the current document builder position.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | Name of the bookmark. |

**Returns:**
[BookmarkStart](../../com.aspose.words/bookmarkstart) - The bookmark start node that was just created.
### startEditableRange() {#startEditableRange--}
```
public EditableRangeStart startEditableRange()
```


Marks the current position in the document as an editable range start.

Editable range in a document can overlap and span any range. To create a valid editable range you need to call both [startEditableRange()](../../com.aspose.words/documentbuilder\#startEditableRange--) and [endEditableRange()](../../com.aspose.words/documentbuilder\#endEditableRange--) or [endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder\#endEditableRange-com.aspose.words.EditableRangeStart-) methods.

Badly formed editable range will be ignored when the document is saved.

**Returns:**
[EditableRangeStart](../../com.aspose.words/editablerangestart) - The editable range start node that was just created.
### startTable() {#startTable--}
```
public Table startTable()
```


Starts a table in the document.

The next method to call is [insertCell()](../../com.aspose.words/documentbuilder\#insertCell--).

This method starts a nested table when called inside a cell.

**Returns:**
[Table](../../com.aspose.words/table) - The table node that was just created.
### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

### write(String text) {#write-java.lang.String-}
```
public void write(String text)
```


Inserts a string into the document at the current insert position. Current font formatting specified by the [getFont()](../../com.aspose.words/documentbuilder\#getFont--) property is used.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| text | java.lang.String | The string to insert into the document. |

### writeln() {#writeln--}
```
public void writeln()
```


Inserts a paragraph break into the document.

Calls [insertParagraph()](../../com.aspose.words/documentbuilder\#insertParagraph--).

### writeln(String text) {#writeln-java.lang.String-}
```
public void writeln(String text)
```


Inserts a string and a paragraph break into the document. Current font and paragraph formatting specified by the [getFont()](../../com.aspose.words/documentbuilder\#getFont--) and [getParagraphFormat()](../../com.aspose.words/documentbuilder\#getParagraphFormat--) properties are used.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| text | java.lang.String | The string to insert into the document. |

