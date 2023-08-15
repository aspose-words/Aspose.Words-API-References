---
title: DocumentBuilder
linktitle: DocumentBuilder
second_title: Aspose.Words for Java
description: Provides methods to insert text images and other content specify font paragraph and section formatting in Java.
type: docs
weight: 134
url: /java/com.aspose.words/documentbuilder/
---

**Inheritance:**
java.lang.Object
```
public class DocumentBuilder
```

Provides methods to insert text, images and other content, specify font, paragraph and section formatting.

To learn more, visit the [ Document Builder Overview ][Document Builder Overview] documentation article.

 **Remarks:** 

[DocumentBuilder](../../com.aspose.words/documentbuilder/) makes the process of building a [Document](../../com.aspose.words/document/) easier. [Document](../../com.aspose.words/document/) is a composite object consisting of a tree of nodes and while inserting content nodes directly into the tree is possible, it requires good understanding of the tree structure. [DocumentBuilder](../../com.aspose.words/documentbuilder/) is a "facade" for the complex structure of [Document](../../com.aspose.words/document/) and allows to insert content and formatting quickly and easily.

Create a [DocumentBuilder](../../com.aspose.words/documentbuilder/) and associate it with a [Document](../../com.aspose.words/document/).

The [DocumentBuilder](../../com.aspose.words/documentbuilder/) has an internal cursor where the text will be inserted when you call [write(java.lang.String)](../../com.aspose.words/documentbuilder/\#write-java.lang.String), [writeln(java.lang.String)](../../com.aspose.words/documentbuilder/\#writeln-java.lang.String), **M:Aspose.Words.DocumentBuilder.InsertBreak(Aspose.Words.BreakType)** and other methods. You can navigate the [DocumentBuilder](../../com.aspose.words/documentbuilder/) cursor to a different location in a document using various MoveToXXX methods.

Use the [getFont()](../../com.aspose.words/documentbuilder/\#getFont) property to specify character formatting that will apply to all text inserted from the current position in the document onwards.

Use the [getParagraphFormat()](../../com.aspose.words/documentbuilder/\#getParagraphFormat) property to specify paragraph formatting for the current and all paragraphs that will be inserted.

Use the [getPageSetup()](../../com.aspose.words/documentbuilder/\#getPageSetup) property to specify page and section properties for the current section and all section that will be inserted.

Use the [getCellFormat()](../../com.aspose.words/documentbuilder/\#getCellFormat) and [getRowFormat()](../../com.aspose.words/documentbuilder/\#getRowFormat) properties to specify formatting properties for table cells and rows. User the [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell) and [endRow()](../../com.aspose.words/documentbuilder/\#endRow) methods to build a table.

Note that [getFont()](../../com.aspose.words/documentbuilder/\#getFont), [getParagraphFormat()](../../com.aspose.words/documentbuilder/\#getParagraphFormat) and [getPageSetup()](../../com.aspose.words/documentbuilder/\#getPageSetup) properties are updated whenever you navigate to a different place in the document to reflect formatting properties available at the new location.

 **Examples:** 

Shows how to use a document builder to create a table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Start the table, then populate the first row with two cells.
 builder.startTable();
 builder.insertCell();
 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");

 // Call the builder's "EndRow" method to start a new row.
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateTable.docx");
 
```

Shows how to create headers and footers in a document using DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

Shows how to build a table with custom borders.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```


[Document Builder Overview]: https://docs.aspose.com/words/java/document-builder-overview/
## Constructors

| Constructor | Description |
| --- | --- |
| [DocumentBuilder()](#DocumentBuilder) | Initializes a new instance of this class. |
| [DocumentBuilder(Document doc)](#DocumentBuilder-com.aspose.words.Document) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [clearCellAttrs()](#clearCellAttrs) |  |
| [clearParaAttrs()](#clearParaAttrs) |  |
| [clearRowAttrs()](#clearRowAttrs) |  |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [deleteRow(int tableIndex, int rowIndex)](#deleteRow-int-int) | Deletes a row from a table. |
| [endBookmark(String bookmarkName)](#endBookmark-java.lang.String) | Marks the current position in the document as a bookmark end. |
| [endColumnBookmark(String bookmarkName)](#endColumnBookmark-java.lang.String) | Marks the current position in the document as a column bookmark end. |
| [endEditableRange()](#endEditableRange) | Marks the current position in the document as an editable range end. |
| [endEditableRange(EditableRangeStart start)](#endEditableRange-com.aspose.words.EditableRangeStart) | Marks the current position in the document as an editable range end. |
| [endRow()](#endRow) | Ends a table row in the document. |
| [endTable()](#endTable) | Ends a table in the document. |
| [fetchCellAttr(int key)](#fetchCellAttr-int) |  |
| [fetchInheritedCellAttr(int key)](#fetchInheritedCellAttr-int) |  |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int) |  |
| [fetchInheritedRowAttr(int key)](#fetchInheritedRowAttr-int) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int) |  |
| [fetchRowAttr(int key)](#fetchRowAttr-int) |  |
| [getBold()](#getBold) | True if the font is formatted as bold. |
| [getCellFormat()](#getCellFormat) | Returns an object that represents current table cell formatting properties. |
| [getCurrentNode()](#getCurrentNode) | Gets the node that is currently selected in this DocumentBuilder. |
| [getCurrentParagraph()](#getCurrentParagraph) | Gets the paragraph that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/). |
| [getCurrentSection()](#getCurrentSection) | Gets the section that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/). |
| [getCurrentStory()](#getCurrentStory) | Gets the story that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/). |
| [getCurrentStructuredDocumentTag()](#getCurrentStructuredDocumentTag) | Gets the structured document tag that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/). |
| [getDirectCellAttr(int key)](#getDirectCellAttr-int) |  |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int) |  |
| [getDirectRowAttr(int key)](#getDirectRowAttr-int) |  |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getDocument()](#getDocument) | Gets the [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) object that this object is attached to. |
| [getFont()](#getFont) | Returns an object that represents current font formatting properties. |
| [getItalic()](#getItalic) | True if the font is formatted as italic. |
| [getListFormat()](#getListFormat) | Returns an object that represents current list formatting properties. |
| [getPageSetup()](#getPageSetup) | Returns an object that represents current page setup and section properties. |
| [getParagraphFormat()](#getParagraphFormat) | Returns an object that represents current paragraph formatting properties. |
| [getRowFormat()](#getRowFormat) | Returns an object that represents current table row formatting properties. |
| [getUnderline()](#getUnderline) | Gets/sets underline type for the current font. |
| [insertBreak(int breakType)](#insertBreak-int) |  |
| [insertCell()](#insertCell) | Inserts a table cell into the document. |
| [insertChart(int chartType, double width, double height)](#insertChart-int-double-double) |  |
| [insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertChart-int-int-double-int-double-double-double-int) |  |
| [insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size)](#insertCheckBox-java.lang.String-boolean-boolean-int) | Inserts a checkbox form field at the current position. |
| [insertCheckBox(String name, boolean checkedValue, int size)](#insertCheckBox-java.lang.String-boolean-int) | Inserts a checkbox form field at the current position. |
| [insertComboBox(String name, String[] items, int selectedIndex)](#insertComboBox-java.lang.String-java.lang.String---int) | Inserts a combobox form field at the current position. |
| [insertDocument(Document srcDoc, int importFormatMode)](#insertDocument-com.aspose.words.Document-int) |  |
| [insertDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#insertDocument-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions) |  |
| [insertField(int fieldType, boolean updateField)](#insertField-int-boolean) |  |
| [insertField(String fieldCode)](#insertField-java.lang.String) | Inserts a Word field into a document and updates the field result. |
| [insertField(String fieldCode, String fieldValue)](#insertField-java.lang.String-java.lang.String) | Inserts a Word field into a document without updating the field result. |
| [insertFootnote(int footnoteType, String footnoteText)](#insertFootnote-int-java.lang.String) |  |
| [insertFootnote(int footnoteType, String footnoteText, String referenceMark)](#insertFootnote-int-java.lang.String-java.lang.String) |  |
| [insertHorizontalRule()](#insertHorizontalRule) | Inserts a horizontal rule shape into the document. |
| [insertHtml(String html)](#insertHtml-java.lang.String) | Inserts an HTML string into the document. |
| [insertHtml(String html, boolean useBuilderFormatting)](#insertHtml-java.lang.String-boolean) | Inserts an HTML string into the document. |
| [insertHtml(String html, int options)](#insertHtml-java.lang.String-int) |  |
| [insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark)](#insertHyperlink-java.lang.String-java.lang.String-boolean) | Inserts a hyperlink into the document. |
| [insertImage(byte[] imageBytes)](#insertImage-byte) | Inserts an image from a byte array into the document. |
| [insertImage(byte[] imageBytes, double width, double height)](#insertImage-byte---double-double) | Inserts an inline image from a byte array into the document and scales it to the specified size. |
| [insertImage(byte[] imageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-byte---int-double-int-double-double-double-int) |  |
| [insertImage(BufferedImage image)](#insertImage-java.awt.image.BufferedImage) | Inserts an image into the document. |
| [insertImage(BufferedImage image, double width, double height)](#insertImage-java.awt.image.BufferedImage-double-double) | Inserts an inline image from a  object into the document and scales it to the specified size. |
| [insertImage(BufferedImage image, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.awt.image.BufferedImage-int-double-int-double-double-double-int) |  |
| [insertImage(InputStream stream)](#insertImage-java.io.InputStream) |  |
| [insertImage(InputStream stream, double width, double height)](#insertImage-java.io.InputStream-double-double) |  |
| [insertImage(InputStream stream, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.io.InputStream-int-double-int-double-double-double-int) |  |
| [insertImage(String fileName)](#insertImage-java.lang.String) | Inserts an image from a file or URL into the document. |
| [insertImage(String fileName, double width, double height)](#insertImage-java.lang.String-double-double) | Inserts an inline image from a file or URL into the document and scales it to the specified size. |
| [insertImage(String fileName, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.lang.String-int-double-int-double-double-double-int) |  |
| [insertNode(Node node)](#insertNode-com.aspose.words.Node) | Inserts a node before the cursor. |
| [insertOleObject(InputStream stream, String progId, boolean asIcon, InputStream presentation)](#insertOleObject-java.io.InputStream-java.lang.String-boolean-java.io.InputStream) |  |
| [insertOleObject(String fileName, boolean isLinked, boolean asIcon, InputStream presentation)](#insertOleObject-java.lang.String-boolean-boolean-java.io.InputStream) |  |
| [insertOleObject(String fileName, String progId, boolean isLinked, boolean asIcon, InputStream presentation)](#insertOleObject-java.lang.String-java.lang.String-boolean-boolean-java.io.InputStream) |  |
| [insertOleObjectAsIcon(InputStream stream, String progId, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.io.InputStream-java.lang.String-java.lang.String-java.lang.String) |  |
| [insertOleObjectAsIcon(String fileName, boolean isLinked, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.lang.String-boolean-java.lang.String-java.lang.String) | Inserts an embedded or linked OLE object as icon into the document. |
| [insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.lang.String-java.lang.String-boolean-java.lang.String-java.lang.String) | Inserts an embedded or linked OLE object as icon into the document. |
| [insertOnlineVideo(String videoUrl, double width, double height)](#insertOnlineVideo-java.lang.String-double-double) | Inserts an online video object into the document and scales it to the specified size. |
| [insertOnlineVideo(String videoUrl, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertOnlineVideo-java.lang.String-int-double-int-double-double-double-int) |  |
| [insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height)](#insertOnlineVideo-java.lang.String-java.lang.String-byte---double-double) | Inserts an online video object into the document and scales it to the specified size. |
| [insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertOnlineVideo-java.lang.String-java.lang.String-byte---int-double-int-double-double-double-int) |  |
| [insertParagraph()](#insertParagraph) | Inserts a paragraph break into the document. |
| [insertShape(int shapeType, double width, double height)](#insertShape-int-double-double) |  |
| [insertShape(int shapeType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertShape-int-int-double-int-double-double-double-int) |  |
| [insertSignatureLine(SignatureLineOptions signatureLineOptions)](#insertSignatureLine-com.aspose.words.SignatureLineOptions) | Inserts a signature line at the current position. |
| [insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType)](#insertSignatureLine-com.aspose.words.SignatureLineOptions-int-double-int-double-int) |  |
| [insertStyleSeparator()](#insertStyleSeparator) | Inserts style separator into the document. |
| [insertTableOfContents(String switches)](#insertTableOfContents-java.lang.String) | Inserts a TOC (table of contents) field into the document. |
| [insertTextInput(String name, int type, String format, String fieldValue, int maxLength)](#insertTextInput-java.lang.String-int-java.lang.String-java.lang.String-int) |  |
| [isAtEndOfParagraph()](#isAtEndOfParagraph) | Returns  true  if the cursor is at the end of the current paragraph. |
| [isAtEndOfStructuredDocumentTag()](#isAtEndOfStructuredDocumentTag) | Returns **true** if the cursor is at the end of a structured document tag. |
| [isAtStartOfParagraph()](#isAtStartOfParagraph) | Returns  true  if the cursor is at the beginning of the current paragraph (no text before the cursor). |
| [moveTo(Node node)](#moveTo-com.aspose.words.Node) | Moves the cursor to an inline node or to the end of a paragraph. |
| [moveToBookmark(String bookmarkName)](#moveToBookmark-java.lang.String) | Moves the cursor to a bookmark. |
| [moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter)](#moveToBookmark-java.lang.String-boolean-boolean) | Moves the cursor to a bookmark with greater precision. |
| [moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)](#moveToCell-int-int-int-int) | Moves the cursor to a table cell in the current section. |
| [moveToDocumentEnd()](#moveToDocumentEnd) | Moves the cursor to the end of the document. |
| [moveToDocumentStart()](#moveToDocumentStart) | Moves the cursor to the beginning of the document. |
| [moveToField(Field field, boolean isAfter)](#moveToField-com.aspose.words.Field-boolean) | Moves the cursor to a field in the document. |
| [moveToHeaderFooter(int headerFooterType)](#moveToHeaderFooter-int) |  |
| [moveToMergeField(String fieldName)](#moveToMergeField-java.lang.String) | Moves the cursor to the specified merge field. |
| [moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField)](#moveToMergeField-java.lang.String-boolean-boolean) | Moves the merge field to the specified merge field. |
| [moveToParagraph(int paragraphIndex, int characterIndex)](#moveToParagraph-int-int) | Moves the cursor to a paragraph in the current section. |
| [moveToSection(int sectionIndex)](#moveToSection-int) | Moves the cursor to the beginning of the body in a specified section. |
| [moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex)](#moveToStructuredDocumentTag-com.aspose.words.StructuredDocumentTag-int) | Moves the cursor to the structured document tag. |
| [moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)](#moveToStructuredDocumentTag-int-int) | Moves the cursor to a structured document tag in the current section. |
| [popFont()](#popFont) | Retrieves character formatting previously saved on the stack. |
| [pushFont()](#pushFont) | Saves current character formatting onto the stack. |
| [removeParaAttr(int key)](#removeParaAttr-int) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [resetToDefaultAttrs()](#resetToDefaultAttrs) |  |
| [setBold(boolean value)](#setBold-boolean) | True if the font is formatted as bold. |
| [setCellAttr(int key, Object value)](#setCellAttr-int-java.lang.Object) |  |
| [setDocument(Document value)](#setDocument-com.aspose.words.Document) | Sets the [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) object that this object is attached to. |
| [setItalic(boolean value)](#setItalic-boolean) | True if the font is formatted as italic. |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object) |  |
| [setRowAttr(int key, Object value)](#setRowAttr-int-java.lang.Object) |  |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [setUnderline(int value)](#setUnderline-int) | Gets/sets underline type for the current font. |
| [startBookmark(String bookmarkName)](#startBookmark-java.lang.String) | Marks the current position in the document as a bookmark start. |
| [startColumnBookmark(String bookmarkName)](#startColumnBookmark-java.lang.String) | Marks the current position in the document as a column bookmark start. |
| [startEditableRange()](#startEditableRange) | Marks the current position in the document as an editable range start. |
| [startTable()](#startTable) | Starts a table in the document. |
| [write(String text)](#write-java.lang.String) | Inserts a string into the document at the current insert position. |
| [writeln()](#writeln) | Inserts a paragraph break into the document. |
| [writeln(String text)](#writeln-java.lang.String) | Inserts a string and a paragraph break into the document. |
### DocumentBuilder() {#DocumentBuilder}
```
public DocumentBuilder()
```


Initializes a new instance of this class.

 **Remarks:** 

Creates a new [DocumentBuilder](../../com.aspose.words/documentbuilder/) object and attaches it to a new [Document](../../com.aspose.words/document/) object.

 **Examples:** 

Shows how to insert formatted text using DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

### DocumentBuilder(Document doc) {#DocumentBuilder-com.aspose.words.Document}
```
public DocumentBuilder(Document doc)
```


Initializes a new instance of this class.

 **Remarks:** 

Creates a new [DocumentBuilder](../../com.aspose.words/documentbuilder/) object, attaches to the specified [Document](../../com.aspose.words/document/) object. The cursor is positioned at the beginning of the document.

 **Examples:** 

Shows how to create headers and footers in a document using DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

Shows how to insert a Table of contents (TOC) into a document using heading styles as entries.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a table of contents for the first page of the document.
 // Configure the table to pick up paragraphs with headings of levels 1 to 3.
 // Also, set its entries to be hyperlinks that will take us
 // to the location of the heading when left-clicked in Microsoft Word.
 builder.insertTableOfContents("\\o \"1-3\" \\h \\z \\u");
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Populate the table of contents by adding paragraphs with heading styles.
 // Each such heading with a level between 1 and 3 will create an entry in the table.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 2");
 builder.writeln("Heading 3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);
 builder.writeln("Heading 3.1.1");
 builder.writeln("Heading 3.1.2");
 builder.writeln("Heading 3.1.3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_4);
 builder.writeln("Heading 3.1.3.1");
 builder.writeln("Heading 3.1.3.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.2");
 builder.writeln("Heading 3.3");

 // A table of contents is a field of a type that needs to be updated to show an up-to-date result.
 doc.updateFields();
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertToc.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) | The [Document](../../com.aspose.words/document/) object to attach to. |

### clearCellAttrs() {#clearCellAttrs}
```
public void clearCellAttrs()
```




### clearParaAttrs() {#clearParaAttrs}
```
public void clearParaAttrs()
```




### clearRowAttrs() {#clearRowAttrs}
```
public void clearRowAttrs()
```




### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### deleteRow(int tableIndex, int rowIndex) {#deleteRow-int-int}
```
public Row deleteRow(int tableIndex, int rowIndex)
```


Deletes a row from a table.

 **Remarks:** 

If the cursor is inside the row that is being deleted, the cursor is moved out to the next row or to the next paragraph after the table.

If you delete a row from a table that contains only one row, the whole table is deleted.

For the index parameters, when index is greater than or equal to 0, it specifies an index from the beginning with 0 being the first element. When index is less than 0, it specified an index from the end with -1 being the last element.

 **Examples:** 

Shows how to delete a row from a table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.write("Row 2, cell 2.");
 builder.endTable();

 Assert.assertEquals(2, table.getRows().getCount());

 // Delete the first row of the first table in the document.
 builder.deleteRow(0, 0);

 Assert.assertEquals(1, table.getRows().getCount());
 Assert.assertEquals("Row 2, cell 1.Row 2, cell 2.", table.getText().trim());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tableIndex | int | The index of the table. |
| rowIndex | int | The index of the row in the table. |

**Returns:**
[Row](../../com.aspose.words/row/) - The row node that was just removed.
### endBookmark(String bookmarkName) {#endBookmark-java.lang.String}
```
public BookmarkEnd endBookmark(String bookmarkName)
```


Marks the current position in the document as a bookmark end.

 **Remarks:** 

Bookmarks in a document can overlap and span any range. To create a valid bookmark you need to call both [startBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#startBookmark-java.lang.String) and [endBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#endBookmark-java.lang.String) with the same  bookmarkName  parameter.

Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.

 **Examples:** 

Shows how create a bookmark.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A valid bookmark needs to have document body text enclosed by
 // BookmarkStart and BookmarkEnd nodes created with a matching bookmark name.
 builder.startBookmark("MyBookmark");
 builder.writeln("Hello world!");
 builder.endBookmark("MyBookmark");

 Assert.assertEquals(1, doc.getRange().getBookmarks().getCount());
 Assert.assertEquals("MyBookmark", doc.getRange().getBookmarks().get(0).getName());
 Assert.assertEquals("Hello world!", doc.getRange().getBookmarks().get(0).getText().trim());
 
```

Shows how to insert a hyperlink which references a local bookmark.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startBookmark("Bookmark1");
 builder.write("Bookmarked text. ");
 builder.endBookmark("Bookmark1");
 builder.writeln("Text outside of the bookmark.");

 // Insert a HYPERLINK field that links to the bookmark. We can pass field switches
 // to the "InsertHyperlink" method as part of the argument containing the referenced bookmark's name.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 builder.insertHyperlink("Link to Bookmark1", "Bookmark1\" \\o \"Hyperlink Tip", true);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | Name of the bookmark. |

**Returns:**
[BookmarkEnd](../../com.aspose.words/bookmarkend/) - The bookmark end node that was just created.
### endColumnBookmark(String bookmarkName) {#endColumnBookmark-java.lang.String}
```
public BookmarkEnd endColumnBookmark(String bookmarkName)
```


Marks the current position in the document as a column bookmark end. The position must be in a table cell.

 **Remarks:** 

A column bookmark covers one or more columns in a range of rows. To create a valid bookmark you need to call both [startColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#startColumnBookmark-java.lang.String) and [endColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#endColumnBookmark-java.lang.String) with the same  bookmarkName  parameter.

Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.

The actual position of the inserted [BookmarkEnd](../../com.aspose.words/bookmarkend/) node may differ from the current document builder position.

 **Examples:** 

Shows how to create a column bookmark.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 builder.insertCell();
 // Cells 1,2,4,5 will be bookmarked.
 builder.startColumnBookmark("MyBookmark_1");
 // Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.
 builder.startColumnBookmark("MyBookmark_1");
 builder.startColumnBookmark("BadStartBookmark");
 builder.write("Cell 1");

 builder.insertCell();
 builder.write("Cell 2");

 builder.insertCell();
 builder.write("Cell 3");

 builder.endRow();

 builder.insertCell();
 builder.write("Cell 4");

 builder.insertCell();
 builder.write("Cell 5");
 builder.endColumnBookmark("MyBookmark_1");
 builder.endColumnBookmark("MyBookmark_1");

 builder.insertCell();
 builder.write("Cell 6");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "Bookmarks.CreateColumnBookmark.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | Name of the bookmark. |

**Returns:**
[BookmarkEnd](../../com.aspose.words/bookmarkend/) - The bookmark end node that was just created.
### endEditableRange() {#endEditableRange}
```
public EditableRangeEnd endEditableRange()
```


Marks the current position in the document as an editable range end.

 **Remarks:** 

Editable range in a document can overlap and span any range. To create a valid editable range you need to call both [startEditableRange()](../../com.aspose.words/documentbuilder/\#startEditableRange) and [endEditableRange()](../../com.aspose.words/documentbuilder/\#endEditableRange) or [endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder/\#endEditableRange-com.aspose.words.EditableRangeStart) methods.

Badly formed editable range will be ignored when the document is saved.

 **Examples:** 

Shows how to work with an editable range.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "MyPassword");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! Since we have set the document's protection level to read-only," +
         " we cannot edit this paragraph without the password.");

 // Editable ranges allow us to leave parts of protected documents open for editing.
 EditableRangeStart editableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph is inside an editable range, and can be edited.");
 EditableRangeEnd editableRangeEnd = builder.endEditableRange();

 // A well-formed editable range has a start node, and end node.
 // These nodes have matching IDs and encompass editable nodes.
 EditableRange editableRange = editableRangeStart.getEditableRange();

 Assert.assertEquals(editableRangeStart.getId(), editableRange.getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getId());

 // Different parts of the editable range link to each other.
 Assert.assertEquals(editableRangeStart.getId(), editableRange.getEditableRangeStart().getId());
 Assert.assertEquals(editableRangeStart.getId(), editableRangeEnd.getEditableRangeStart().getId());
 Assert.assertEquals(editableRange.getId(), editableRangeStart.getEditableRange().getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getEditableRangeEnd().getId());

 // We can access the node types of each part like this. The editable range itself is not a node,
 // but an entity which consists of a start, an end, and their enclosed contents.
 Assert.assertEquals(NodeType.EDITABLE_RANGE_START, editableRangeStart.getNodeType());
 Assert.assertEquals(NodeType.EDITABLE_RANGE_END, editableRangeEnd.getNodeType());

 builder.writeln("This paragraph is outside the editable range, and cannot be edited.");

 doc.save(getArtifactsDir() + "EditableRange.CreateAndRemove.docx");

 // Remove an editable range. All the nodes that were inside the range will remain intact.
 editableRange.remove();
 
```

**Returns:**
[EditableRangeEnd](../../com.aspose.words/editablerangeend/) - The editable range end node that was just created.
### endEditableRange(EditableRangeStart start) {#endEditableRange-com.aspose.words.EditableRangeStart}
```
public EditableRangeEnd endEditableRange(EditableRangeStart start)
```


Marks the current position in the document as an editable range end.

 **Remarks:** 

Use this overload during creating nested editable ranges.

Editable range in a document can overlap and span any range. To create a valid editable range you need to call both [startEditableRange()](../../com.aspose.words/documentbuilder/\#startEditableRange) and [endEditableRange()](../../com.aspose.words/documentbuilder/\#endEditableRange) or [endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder/\#endEditableRange-com.aspose.words.EditableRangeStart) methods.

Badly formed editable range will be ignored when the document is saved.

 **Examples:** 

Shows how to create nested editable ranges.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "MyPassword");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! Since we have set the document's protection level to read-only, " +
         "we cannot edit this paragraph without the password.");

 // Create two nested editable ranges.
 EditableRangeStart outerEditableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph inside the outer editable range and can be edited.");

 EditableRangeStart innerEditableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

 // Currently, the document builder's node insertion cursor is in more than one ongoing editable range.
 // When we want to end an editable range in this situation,
 // we need to specify which of the ranges we wish to end by passing its EditableRangeStart node.
 builder.endEditableRange(innerEditableRangeStart);

 builder.writeln("This paragraph inside the outer editable range and can be edited.");

 builder.endEditableRange(outerEditableRangeStart);

 builder.writeln("This paragraph is outside any editable ranges, and cannot be edited.");

 // If a region of text has two overlapping editable ranges with specified groups,
 // the combined group of users excluded by both groups are prevented from editing it.
 outerEditableRangeStart.getEditableRange().setEditorGroup(EditorType.EVERYONE);
 innerEditableRangeStart.getEditableRange().setEditorGroup(EditorType.CONTRIBUTORS);

 doc.save(getArtifactsDir() + "EditableRange.Nested.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| start | [EditableRangeStart](../../com.aspose.words/editablerangestart/) | This editable range start. |

**Returns:**
[EditableRangeEnd](../../com.aspose.words/editablerangeend/) - The editable range end node that was just created.
### endRow() {#endRow}
```
public Row endRow()
```


Ends a table row in the document.

 **Remarks:** 

Call [endRow()](../../com.aspose.words/documentbuilder/\#endRow) to end a table row. If you call [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell) immediately after that, then the table continues on a new row.

Use the [getRowFormat()](../../com.aspose.words/documentbuilder/\#getRowFormat) property to specify row formatting.

 **Examples:** 

Shows how to merge table cells vertically.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a cell into the first column of the first row.
 // This cell will be the first in a range of vertically merged cells.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.FIRST);
 builder.write("Text in merged cells.");

 // Insert a cell into the second column of the first row, then end the row.
 // Also, configure the builder to disable vertical merging in created cells.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.NONE);
 builder.write("Text in unmerged cell.");
 builder.endRow();

 // Insert a cell into the first column of the second row.
 // Instead of adding text contents, we will merge this cell with the first cell that we added directly above.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.PREVIOUS);

 // Insert another independent cell in the second column of the second row.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.NONE);
 builder.write("Text in unmerged cell.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "CellFormat.VerticalMerge.docx");
 
```

Shows how to build a table with custom borders.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Shows how to build a formatted 2x2 table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

**Returns:**
[Row](../../com.aspose.words/row/) - The row node that was just finished.
### endTable() {#endTable}
```
public Table endTable()
```


Ends a table in the document.

 **Remarks:** 

This method should be called only once after [endRow()](../../com.aspose.words/documentbuilder/\#endRow) was called. When called, [endTable()](../../com.aspose.words/documentbuilder/\#endTable) moves the cursor out of the current cell to point just after the table.

 **Examples:** 

Shows how to build a table with custom borders.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Shows how to format cells with a document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

Shows how to build a formatted 2x2 table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

**Returns:**
[Table](../../com.aspose.words/table/) - The table node that was just finished.
### fetchCellAttr(int key) {#fetchCellAttr-int}
```
public Object fetchCellAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedCellAttr(int key) {#fetchInheritedCellAttr-int}
```
public Object fetchInheritedCellAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int}
```
public Object fetchInheritedParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRowAttr(int key) {#fetchInheritedRowAttr-int}
```
public Object fetchInheritedRowAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRunAttr(int fontAttr) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int fontAttr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### fetchParaAttr(int key) {#fetchParaAttr-int}
```
public Object fetchParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchRowAttr(int key) {#fetchRowAttr-int}
```
public Object fetchRowAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getBold() {#getBold}
```
public boolean getBold()
```


True if the font is formatted as bold.

 **Examples:** 

Shows how to fill MERGEFIELDs with data with a document builder instead of a mail merge.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
 // and then fill them manually.
 builder.insertField(" MERGEFIELD Chairman ");
 builder.insertField(" MERGEFIELD ChiefFinancialOfficer ");
 builder.insertField(" MERGEFIELD ChiefTechnologyOfficer ");

 builder.moveToMergeField("Chairman");
 builder.setBold(true);
 builder.writeln("John Doe");

 builder.moveToMergeField("ChiefFinancialOfficer");
 builder.setItalic(true);
 builder.writeln("Jane Doe");

 builder.moveToMergeField("ChiefTechnologyOfficer");
 builder.setItalic(true);
 builder.writeln("John Bloggs");

 doc.save(getArtifactsDir() + "DocumentBuilder.FillMergeFields.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getCellFormat() {#getCellFormat}
```
public CellFormat getCellFormat()
```


Returns an object that represents current table cell formatting properties.

 **Examples:** 

Shows how to build a table with custom borders.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Shows how to format cells with a document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

Shows how to build a formatted 2x2 table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

**Returns:**
[CellFormat](../../com.aspose.words/cellformat/) - An object that represents current table cell formatting properties.
### getCurrentNode() {#getCurrentNode}
```
public Node getCurrentNode()
```


Gets the node that is currently selected in this DocumentBuilder.

 **Remarks:** 

[getCurrentNode()](../../com.aspose.words/documentbuilder/\#getCurrentNode) is a cursor of [DocumentBuilder](../../com.aspose.words/documentbuilder/) and points to a [Node](../../com.aspose.words/node/) that is a direct child of a [Paragraph](../../com.aspose.words/paragraph/). Any insert operations you perform using [DocumentBuilder](../../com.aspose.words/documentbuilder/) will insert before the [getCurrentNode()](../../com.aspose.words/documentbuilder/\#getCurrentNode).

When the current paragraph is empty or the cursor is positioned just before the end of a paragraph or structured document tag, [getCurrentNode()](../../com.aspose.words/documentbuilder/\#getCurrentNode) returns  null .

 **Examples:** 

Shows how to move a document builder's cursor to different nodes in a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The node that is currently selected in this DocumentBuilder.
### getCurrentParagraph() {#getCurrentParagraph}
```
public Paragraph getCurrentParagraph()
```


Gets the paragraph that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/).

 **Remarks:** 

[getCurrentNode()](../../com.aspose.words/documentbuilder/\#getCurrentNode)

 **Examples:** 

Shows how to move a document builder's cursor to different nodes in a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

**Returns:**
[Paragraph](../../com.aspose.words/paragraph/) - The paragraph that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/).
### getCurrentSection() {#getCurrentSection}
```
public Section getCurrentSection()
```


Gets the section that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/).

 **Examples:** 

Shows how to insert a floating image, and specify its position and size.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);

 // Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
 // as the shape's horizontal distance, in points, from the left side of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);

 // Set the shape's horizontal distance from the left side of the page to 100.
 shape.setLeft(100.0);

 // Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setTop(80.0);

 // Set the shape's height, which will automatically scale the width to preserve dimensions.
 shape.setHeight(125.0);

 Assert.assertEquals(125.0d, shape.getWidth());

 // The "Bottom" and "Right" properties contain the bottom and right edges of the image.
 Assert.assertEquals(shape.getTop() + shape.getHeight(), shape.getBottom());
 Assert.assertEquals(shape.getLeft() + shape.getWidth(), shape.getRight());

 doc.save(getArtifactsDir() + "Image.CreateFloatingPositionSize.docx");
 
```

**Returns:**
[Section](../../com.aspose.words/section/) - The section that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/).
### getCurrentStory() {#getCurrentStory}
```
public Story getCurrentStory()
```


Gets the story that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/).

 **Examples:** 

Shows how to work with a document builder's current story.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A Story is a type of node that has child Paragraph nodes, such as a Body.
 Assert.assertEquals(builder.getCurrentStory(), doc.getFirstSection().getBody());
 Assert.assertEquals(builder.getCurrentStory(), builder.getCurrentParagraph().getParentNode());
 Assert.assertEquals(StoryType.MAIN_TEXT, builder.getCurrentStory().getStoryType());

 builder.getCurrentStory().appendParagraph("Text added to current Story.");

 // A Story can also contain tables.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1");
 builder.insertCell();
 builder.write("Row 1, cell 2");
 builder.endTable();

 Assert.assertTrue(builder.getCurrentStory().getTables().contains(table));
 
```

**Returns:**
[Story](../../com.aspose.words/story/) - The story that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/).
### getCurrentStructuredDocumentTag() {#getCurrentStructuredDocumentTag}
```
public StructuredDocumentTag getCurrentStructuredDocumentTag()
```


Gets the structured document tag that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/).

 **Examples:** 

Shows how to move cursor of DocumentBuilder inside a structured document tag.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 // There is a several ways to move the cursor:
 // 1 -  Move to the first character of structured document tag by index.
 builder.moveToStructuredDocumentTag(1, 1);

 // 2 -  Move to the first character of structured document tag by object.
 StructuredDocumentTag tag = (StructuredDocumentTag)doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG, 2, true);
 builder.moveToStructuredDocumentTag(tag, 1);
 builder.write(" New text.");

 Assert.assertEquals("R New text.ichText", tag.getText().trim());

 // 3 -  Move to the end of the second structured document tag.
 builder.moveToStructuredDocumentTag(1, -1);
 Assert.assertTrue(builder.isAtEndOfStructuredDocumentTag());

 // Get currently selected structured document tag.
 builder.getCurrentStructuredDocumentTag().setColor(Color.GREEN);

 doc.save(getArtifactsDir() + "Document.MoveToStructuredDocumentTag.docx");
 
```

**Returns:**
[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) - The structured document tag that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/).
### getDirectCellAttr(int key) {#getDirectCellAttr-int}
```
public Object getDirectCellAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key) {#getDirectParaAttr-int}
```
public Object getDirectParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int}
```
public Object getDirectParaAttr(int key, int revisionsView)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDirectRowAttr(int key) {#getDirectRowAttr-int}
```
public Object getDirectRowAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int fontAttr) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int fontAttr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDocument() {#getDocument}
```
public Document getDocument()
```


Gets the [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) object that this object is attached to.

 **Examples:** 

Shows how to apply and revert page setup settings to sections in a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

**Returns:**
[Document](../../com.aspose.words/document/) - The [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) object that this object is attached to.
### getFont() {#getFont}
```
public Font getFont()
```


Returns an object that represents current font formatting properties.

 **Remarks:** 

Use [getFont()](../../com.aspose.words/documentbuilder/\#getFont) to access and modify font formatting properties.

Specify font formatting before inserting text.

 **Examples:** 

Shows how to insert a string surrounded by a border into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

Shows how to create a formatted table using DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 table.setLeftIndent(20.0);

 // Set some formatting options for text and table appearance.
 builder.getRowFormat().setHeight(40.0);
 builder.getRowFormat().setHeightRule(HeightRule.AT_LEAST);
 builder.getCellFormat().getShading().setBackgroundPatternColor(new Color((198), (217), (241)));

 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.getFont().setSize(16.0);
 builder.getFont().setName("Arial");
 builder.getFont().setBold(true);

 // Configuring the formatting options in a document builder will apply them
 // to the current cell/row its cursor is in,
 // as well as any new cells and rows created using that builder.
 builder.write("Header Row,\n Cell 1");
 builder.insertCell();
 builder.write("Header Row,\n Cell 2");
 builder.insertCell();
 builder.write("Header Row,\n Cell 3");
 builder.endRow();

 // Reconfigure the builder's formatting objects for new rows and cells that we are about to make.
 // The builder will not apply these to the first row already created so that it will stand out as a header row.
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.WHITE);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getRowFormat().setHeight(30.0);
 builder.getRowFormat().setHeightRule(HeightRule.AUTO);
 builder.insertCell();
 builder.getFont().setSize(12.0);
 builder.getFont().setBold(false);

 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");
 builder.insertCell();
 builder.write("Row 1, Cell 3.");
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.insertCell();
 builder.write("Row 2, Cell 3.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateFormattedTable.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - An object that represents current font formatting properties.
### getItalic() {#getItalic}
```
public boolean getItalic()
```


True if the font is formatted as italic.

 **Examples:** 

Shows how to fill MERGEFIELDs with data with a document builder instead of a mail merge.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
 // and then fill them manually.
 builder.insertField(" MERGEFIELD Chairman ");
 builder.insertField(" MERGEFIELD ChiefFinancialOfficer ");
 builder.insertField(" MERGEFIELD ChiefTechnologyOfficer ");

 builder.moveToMergeField("Chairman");
 builder.setBold(true);
 builder.writeln("John Doe");

 builder.moveToMergeField("ChiefFinancialOfficer");
 builder.setItalic(true);
 builder.writeln("Jane Doe");

 builder.moveToMergeField("ChiefTechnologyOfficer");
 builder.setItalic(true);
 builder.writeln("John Bloggs");

 doc.save(getArtifactsDir() + "DocumentBuilder.FillMergeFields.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getListFormat() {#getListFormat}
```
public ListFormat getListFormat()
```


Returns an object that represents current list formatting properties.

 **Examples:** 

Shows how to create bulleted and numbered lists.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Aspose.Words main advantages are:");

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Below are two types of lists that we can create with a document builder.
 // 1 -  A bulleted list:
 // This list will apply an indent and a bullet symbol ("\ufffd") before each paragraph.
 builder.getListFormat().applyBulletDefault();
 builder.writeln("Great performance");
 builder.writeln("High reliability");
 builder.writeln("Quality code and working");
 builder.writeln("Wide variety of features");
 builder.writeln("Easy to understand API");

 // End the bulleted list.
 builder.getListFormat().removeNumbers();

 builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 builder.writeln("Aspose.Words allows:");

 // 2 -  A numbered list:
 // Numbered lists create a logical order for their paragraphs by numbering each item.
 builder.getListFormat().applyNumberDefault();

 // This paragraph is the first item. The first item of a numbered list will have a "1." as its list item symbol.
 builder.writeln("Opening documents from different formats:");

 Assert.assertEquals(0, builder.getListFormat().getListLevelNumber());

 // Call the "ListIndent" method to increase the current list level,
 // which will start a new self-contained list, with a deeper indent, at the current item of the first list level.
 builder.getListFormat().listIndent();

 Assert.assertEquals(1, builder.getListFormat().getListLevelNumber());

 // These are the first three list items of the second list level, which will maintain a count
 // independent of the count of the first list level. According to the current list format,
 // they will have symbols of "a.", "b.", and "c.".
 builder.writeln("DOC");
 builder.writeln("PDF");
 builder.writeln("HTML");

 // Call the "ListOutdent" method to return to the previous list level.
 builder.getListFormat().listOutdent();

 Assert.assertEquals(0, builder.getListFormat().getListLevelNumber());

 // These two paragraphs will continue the count of the first list level.
 // These items will have symbols of "2.", and "3."
 builder.writeln("Processing documents");
 builder.writeln("Saving documents in different formats:");

 // If we increase the list level to a level that we have added items to previously,
 // the nested list will be separate from the previous, and its numbering will start from the beginning.
 // These list items will have symbols of "a.", "b.", "c.", "d.", and "e".
 builder.getListFormat().listIndent();
 builder.writeln("DOC");
 builder.writeln("PDF");
 builder.writeln("HTML");
 builder.writeln("MHTML");
 builder.writeln("Plain text");

 // Outdent the list level again.
 builder.getListFormat().listOutdent();
 builder.writeln("Doing many other things!");

 // End the numbered list.
 builder.getListFormat().removeNumbers();

 doc.save(getArtifactsDir() + "Lists.ApplyDefaultBulletsAndNumbers.docx");
 
```

**Returns:**
[ListFormat](../../com.aspose.words/listformat/) - An object that represents current list formatting properties.
### getPageSetup() {#getPageSetup}
```
public PageSetup getPageSetup()
```


Returns an object that represents current page setup and section properties.

 **Examples:** 

Shows how to apply and revert page setup settings to sections in a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

**Returns:**
[PageSetup](../../com.aspose.words/pagesetup/) - An object that represents current page setup and section properties.
### getParagraphFormat() {#getParagraphFormat}
```
public ParagraphFormat getParagraphFormat()
```


Returns an object that represents current paragraph formatting properties.

 **Examples:** 

Shows how to create a formatted table using DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 table.setLeftIndent(20.0);

 // Set some formatting options for text and table appearance.
 builder.getRowFormat().setHeight(40.0);
 builder.getRowFormat().setHeightRule(HeightRule.AT_LEAST);
 builder.getCellFormat().getShading().setBackgroundPatternColor(new Color((198), (217), (241)));

 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.getFont().setSize(16.0);
 builder.getFont().setName("Arial");
 builder.getFont().setBold(true);

 // Configuring the formatting options in a document builder will apply them
 // to the current cell/row its cursor is in,
 // as well as any new cells and rows created using that builder.
 builder.write("Header Row,\n Cell 1");
 builder.insertCell();
 builder.write("Header Row,\n Cell 2");
 builder.insertCell();
 builder.write("Header Row,\n Cell 3");
 builder.endRow();

 // Reconfigure the builder's formatting objects for new rows and cells that we are about to make.
 // The builder will not apply these to the first row already created so that it will stand out as a header row.
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.WHITE);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getRowFormat().setHeight(30.0);
 builder.getRowFormat().setHeightRule(HeightRule.AUTO);
 builder.insertCell();
 builder.getFont().setSize(12.0);
 builder.getFont().setBold(false);

 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");
 builder.insertCell();
 builder.write("Row 1, Cell 3.");
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.insertCell();
 builder.write("Row 2, Cell 3.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateFormattedTable.docx");
 
```

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat/) - An object that represents current paragraph formatting properties.
### getRowFormat() {#getRowFormat}
```
public RowFormat getRowFormat()
```


Returns an object that represents current table row formatting properties.

 **Examples:** 

Shows how to format rows with a document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Start a second row, and then configure its height. The builder will apply these settings to
 // its current row, as well as any new rows it creates afterwards.
 builder.endRow();

 RowFormat rowFormat = builder.getRowFormat();
 rowFormat.setHeight(100.0);
 rowFormat.setHeightRule(HeightRule.EXACTLY);

 builder.insertCell();
 builder.write("Row 2, cell 1.");
 builder.endTable();

 // The first row was unaffected by the padding reconfiguration and still holds the default values.
 Assert.assertEquals(0.0d, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());

 Assert.assertEquals(100.0d, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());

 doc.save(getArtifactsDir() + "DocumentBuilder.SetRowFormatting.docx");
 
```

Shows how to build a table with custom borders.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Shows how to build a formatted 2x2 table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

**Returns:**
[RowFormat](../../com.aspose.words/rowformat/) - An object that represents current table row formatting properties.
### getUnderline() {#getUnderline}
```
public int getUnderline()
```


Gets/sets underline type for the current font.

 **Examples:** 

Shows how to format text inserted by a document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.setUnderline(Underline.DASH);
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setSize(32.0);

 // The builder applies formatting to its current paragraph and any new text added by it afterward.
 builder.writeln("Large, blue, and underlined text.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertUnderline.docx");
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [Underline](../../com.aspose.words/underline/) constants.
### insertBreak(int breakType) {#insertBreak-int}
```
public void insertBreak(int breakType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| breakType | int |  |

### insertCell() {#insertCell}
```
public Cell insertCell()
```


Inserts a table cell into the document.

 **Remarks:** 

To start a table, just call [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell). After this, any content you add using other methods of the [DocumentBuilder](../../com.aspose.words/documentbuilder/) class will be added to the current cell.

To start a new cell in the same row, call [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell) again.

To end a table row call [endRow()](../../com.aspose.words/documentbuilder/\#endRow).

Use the [getCellFormat()](../../com.aspose.words/documentbuilder/\#getCellFormat) property to specify cell formatting.

 **Examples:** 

Shows how to use a document builder to create a table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Start the table, then populate the first row with two cells.
 builder.startTable();
 builder.insertCell();
 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");

 // Call the builder's "EndRow" method to start a new row.
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateTable.docx");
 
```

Shows how to build a table with custom borders.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

**Returns:**
[Cell](../../com.aspose.words/cell/) - The cell node that was just inserted.
### insertChart(int chartType, double width, double height) {#insertChart-int-double-double}
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
[Shape](../../com.aspose.words/shape/)
### insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertChart-int-int-double-int-double-double-double-int}
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
[Shape](../../com.aspose.words/shape/)
### insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size) {#insertCheckBox-java.lang.String-boolean-boolean-int}
```
public FormField insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size)
```


Inserts a checkbox form field at the current position.

 **Remarks:** 

If you specify a name for the form field, then a bookmark is automatically created with the same name.

 **Examples:** 

Shows how to insert checkboxes into the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert checkboxes of varying sizes and default checked statuses.
 builder.write("Unchecked check box of a default size: ");
 builder.insertCheckBox("", false, false, 0);
 builder.insertParagraph();

 builder.write("Large checked check box: ");
 builder.insertCheckBox("CheckBox_Default", true, true, 50);
 builder.insertParagraph();

 // Form fields have a name length limit of 20 characters.
 builder.write("Very large checked check box: ");
 builder.insertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

 Assert.assertEquals("CheckBox_OnlyChecked", doc.getRange().getFormFields().get(2).getName());

 // We can interact with these check boxes in Microsoft Word by double clicking them.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCheckBox.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the form field. Can be an empty string. The value longer than 20 characters will be truncated. |
| defaultValue | boolean | Default value of the checkbox form field. |
| checkedValue | boolean | Current checked status of the checkbox form field. |
| size | int | Specifies the size of the checkbox in points. Specify 0 for MS Word to calculate the size of the checkbox automatically. |

**Returns:**
[FormField](../../com.aspose.words/formfield/) - The form field node that was just inserted.
### insertCheckBox(String name, boolean checkedValue, int size) {#insertCheckBox-java.lang.String-boolean-int}
```
public FormField insertCheckBox(String name, boolean checkedValue, int size)
```


Inserts a checkbox form field at the current position.

 **Remarks:** 

If you specify a name for the form field, then a bookmark is automatically created with the same name.

 **Examples:** 

Shows how to insert checkboxes into the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert checkboxes of varying sizes and default checked statuses.
 builder.write("Unchecked check box of a default size: ");
 builder.insertCheckBox("", false, false, 0);
 builder.insertParagraph();

 builder.write("Large checked check box: ");
 builder.insertCheckBox("CheckBox_Default", true, true, 50);
 builder.insertParagraph();

 // Form fields have a name length limit of 20 characters.
 builder.write("Very large checked check box: ");
 builder.insertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

 Assert.assertEquals("CheckBox_OnlyChecked", doc.getRange().getFormFields().get(2).getName());

 // We can interact with these check boxes in Microsoft Word by double clicking them.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCheckBox.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the form field. Can be an empty string. The value longer than 20 characters will be truncated. |
| checkedValue | boolean | Checked status of the checkbox form field. |
| size | int | Specifies the size of the checkbox in points. Specify 0 for MS Word to calculate the size of the checkbox automatically. |

**Returns:**
[FormField](../../com.aspose.words/formfield/) - The form field node that was just inserted.
### insertComboBox(String name, String[] items, int selectedIndex) {#insertComboBox-java.lang.String-java.lang.String---int}
```
public FormField insertComboBox(String name, String[] items, int selectedIndex)
```


Inserts a combobox form field at the current position.

 **Remarks:** 

If you specify a name for the form field, then a bookmark is automatically created with the same name.

 **Examples:** 

Shows how to insert a combo box form field into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a form that prompts the user to pick one of the items from the menu.
 builder.write("Pick a fruit: ");
 String[] items = {"Apple", "Banana", "Cherry"};
 builder.insertComboBox("DropDown", items, 0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertComboBox.docx");
 
```

Shows how to create form fields.

```

 DocumentBuilder builder = new DocumentBuilder();

 // Form fields are objects in the document that the user can interact with by being prompted to enter values.
 // We can create them using a document builder, and below are two ways of doing so.
 // 1 -  Basic text input:
 builder.insertTextInput("My text input", TextFormFieldType.REGULAR,
         "", "Enter your name here", 30);

 // 2 -  Combo box with prompt text, and a range of possible values:
 String[] items =
         {
                 "-- Select your favorite footwear --", "Sneakers", "Oxfords", "Flip-flops", "Other"
         };

 builder.insertParagraph();
 builder.insertComboBox("My combo box", items, 0);

 builder.getDocument().save(getArtifactsDir() + "DocumentBuilder.CreateForm.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the form field. Can be an empty string. The value longer than 20 characters will be truncated. |
| items | java.lang.String[] | The items of the ComboBox. Maximum is 25 items. |
| selectedIndex | int | The index of the selected item in the ComboBox. |

**Returns:**
[FormField](../../com.aspose.words/formfield/) - The form field node that was just inserted.
### insertDocument(Document srcDoc, int importFormatMode) {#insertDocument-com.aspose.words.Document-int}
```
public Node insertDocument(Document srcDoc, int importFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document/) |  |
| importFormatMode | int |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### insertDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#insertDocument-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions}
```
public Node insertDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document/) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### insertField(int fieldType, boolean updateField) {#insertField-int-boolean}
```
public Field insertField(int fieldType, boolean updateField)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldType | int |  |
| updateField | boolean |  |

**Returns:**
[Field](../../com.aspose.words/field/)
### insertField(String fieldCode) {#insertField-java.lang.String}
```
public Field insertField(String fieldCode)
```


Inserts a Word field into a document and updates the field result.

 **Remarks:** 

This method inserts a field into a document and updates the field result immediately. Aspose.Words can update fields of most types, but not all. For more details see the [insertField(java.lang.String, java.lang.String)](../../com.aspose.words/documentbuilder/\#insertField-java.lang.String--java.lang.String) overload.

 **Examples:** 

Shows how to insert a field into a document using a field code.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

Shows how to insert fields, and move the document builder's cursor to them.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertField("MERGEFIELD MyMergeField1 \\* MERGEFORMAT");
 builder.insertField("MERGEFIELD MyMergeField2 \\* MERGEFORMAT");

 // Move the cursor to the first MERGEFIELD.
 builder.moveToMergeField("MyMergeField1", true, false);

 // Note that the cursor is placed immediately after the first MERGEFIELD, and before the second.
 Assert.assertEquals(doc.getRange().getFields().get(1).getStart(), builder.getCurrentNode());
 Assert.assertEquals(doc.getRange().getFields().get(0).getEnd(), builder.getCurrentNode().getPreviousSibling());

 // If we wish to edit the field's field code or contents using the builder,
 // its cursor would need to be inside a field.
 // To place it inside a field, we would need to call the document builder's MoveTo method
 // and pass the field's start or separator node as an argument.
 builder.write(" Text between our merge fields. ");

 doc.save(getArtifactsDir() + "DocumentBuilder.MergeFields.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | java.lang.String | The field code to insert (without curly braces). |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the inserted field.
### insertField(String fieldCode, String fieldValue) {#insertField-java.lang.String-java.lang.String}
```
public Field insertField(String fieldCode, String fieldValue)
```


Inserts a Word field into a document without updating the field result.

 **Remarks:** 

Fields in Microsoft Word documents consist of a field code and a field result. The field code is like a formula and the field result is like the value that the formula produces. The field code may also contain field switches that are like additional instructions to perform a specific action.

You can switch between displaying field codes and results in your document in Microsoft Word using the keyboard shortcut Alt+F9. Field codes appear between curly braces ( \{ \} ).

To create a field, you need to specify a field type, field code and a "placeholder" field value. If you are not sure about a particular field code syntax, create the field in Microsoft Word first and switch to see its field code.

Aspose.Words can calculate field results for most of the field types, but this method does not update the field result automatically. Because the field result is not calculated automatically, you are expected to pass some string value (or even an empty string) that will be inserted into the field result. This value will remain in the field result as a placeholder until the field is updated. To update the field result you can call [Field.update()](../../com.aspose.words/field/\#update) on the field object returned to you or [Document.updateFields()](../../com.aspose.words/document/\#updateFields) to update fields in the whole document.

 **Examples:** 

Shows how to set up page numbering in a section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | java.lang.String | The field code to insert (without curly braces). |
| fieldValue | java.lang.String | The field value to insert. Pass  null  for fields that do not have a value. |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the inserted field.
### insertFootnote(int footnoteType, String footnoteText) {#insertFootnote-int-java.lang.String}
```
public Footnote insertFootnote(int footnoteType, String footnoteText)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| footnoteType | int |  |
| footnoteText | java.lang.String |  |

**Returns:**
[Footnote](../../com.aspose.words/footnote/)
### insertFootnote(int footnoteType, String footnoteText, String referenceMark) {#insertFootnote-int-java.lang.String-java.lang.String}
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
[Footnote](../../com.aspose.words/footnote/)
### insertHorizontalRule() {#insertHorizontalRule}
```
public Shape insertHorizontalRule()
```


Inserts a horizontal rule shape into the document.

 **Examples:** 

Shows how to insert a horizontal rule shape, and customize its formatting.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
[Shape](../../com.aspose.words/shape/) - The shape that is a horizontal rule.
### insertHtml(String html) {#insertHtml-java.lang.String}
```
public void insertHtml(String html)
```


Inserts an HTML string into the document.

 **Remarks:** 

You can use this method to insert an HTML fragment or whole HTML document.

 **Examples:** 

Shows how to use a document builder to insert html content into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final String HTML = " Paragraph right" +
         "Implicit paragraph left" +
         " Div center" +
         " Heading 1 left.";

 builder.insertHtml(HTML);

 // Inserting HTML code parses the formatting of each element into equivalent document text formatting.
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals("Paragraph right", paragraphs.get(0).getText().trim());
 Assert.assertEquals(ParagraphAlignment.RIGHT, paragraphs.get(0).getParagraphFormat().getAlignment());

 Assert.assertEquals("Implicit paragraph left", paragraphs.get(1).getText().trim());
 Assert.assertEquals(ParagraphAlignment.LEFT, paragraphs.get(1).getParagraphFormat().getAlignment());
 Assert.assertTrue(paragraphs.get(1).getRuns().get(0).getFont().getBold());

 Assert.assertEquals("Div center", paragraphs.get(2).getText().trim());
 Assert.assertEquals(ParagraphAlignment.CENTER, paragraphs.get(2).getParagraphFormat().getAlignment());

 Assert.assertEquals("Heading 1 left.", paragraphs.get(3).getText().trim());
 Assert.assertEquals("Heading 1", paragraphs.get(3).getParagraphFormat().getStyle().getName());

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHtml.docx");
 
```

Shows how to execute a mail merge with a custom callback that handles merge data in the form of HTML documents.

```

 public void insertHtml() throws Exception {
     Document doc = new Document(getMyDir() + "Field sample - MERGEFIELD.docx");

     // Add a handler for the MergeField event
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeFieldInsertHtml());

     final String htmlText = "\r\n Hello world!\r\n";

     // Execute mail merge
     doc.getMailMerge().execute(new String[]{"htmlField1"}, new String[]{htmlText});

     // Save resulting document with a new name
     doc.save(getArtifactsDir() + "MailMergeEvent.InsertHtml.docx");
 }

 private class HandleMergeFieldInsertHtml implements IFieldMergingCallback {
     // This is called when merge field is actually merged with data in the document.
     public void fieldMerging(final FieldMergingArgs args) throws Exception {
         // All merge fields that expect HTML data should be marked with some prefix, e.g. 'html'
         if (args.getDocumentFieldName().startsWith("html") && args.getField().getFieldCode().contains("\\b")) {
             FieldMergeField field = args.getField();

             // Insert the text for this merge field as HTML data, using DocumentBuilder
             DocumentBuilder builder = new DocumentBuilder(args.getDocument());
             builder.moveToMergeField(args.getDocumentFieldName());
             builder.write(field.getTextBefore());
             builder.insertHtml((String) args.getFieldValue());

             // The HTML text itself should not be inserted
             // We have already inserted it as an HTML
             args.setText("");
         }
     }

     public void imageFieldMerging(ImageFieldMergingArgs args) {
         // Do nothing
     }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| html | java.lang.String | An HTML string to insert into the document. |

### insertHtml(String html, boolean useBuilderFormatting) {#insertHtml-java.lang.String-boolean}
```
public void insertHtml(String html, boolean useBuilderFormatting)
```


Inserts an HTML string into the document.

 **Remarks:** 

You can use this method to insert an HTML fragment or whole HTML document.

When  useBuilderFormatting  is  false , [DocumentBuilder](../../com.aspose.words/documentbuilder/) formating is ignored and formatting of inserted text is based on default HTML formatting. As a result, the text looks as it is rendered in browsers.

When  useBuilderFormatting  is  true , formatting of inserted text is based on [DocumentBuilder](../../com.aspose.words/documentbuilder/) formatting, and the text looks as if it were inserted with [write(java.lang.String)](../../com.aspose.words/documentbuilder/\#write-java.lang.String).

 **Examples:** 

Shows how to apply a document builder's formatting while inserting HTML content.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set a text alignment for the builder, insert an HTML paragraph with a specified alignment, and one without.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.DISTRIBUTED);
 builder.insertHtml(
         " Paragraph 1." +
                 " Paragraph 2.", useBuilderFormatting);

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 // The first paragraph has an alignment specified. When InsertHtml parses the HTML code,
 // the paragraph alignment value found in the HTML code always supersedes the document builder's value.
 Assert.assertEquals("Paragraph 1.", paragraphs.get(0).getText().trim());
 Assert.assertEquals(ParagraphAlignment.RIGHT, paragraphs.get(0).getParagraphFormat().getAlignment());

 // The second paragraph has no alignment specified. It can have its alignment value filled in
 // by the builder's value depending on the flag we passed to the InsertHtml method.
 Assert.assertEquals("Paragraph 2.", paragraphs.get(1).getText().trim());
 Assert.assertEquals(useBuilderFormatting ? ParagraphAlignment.DISTRIBUTED : ParagraphAlignment.LEFT,
         paragraphs.get(1).getParagraphFormat().getAlignment());

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHtmlWithFormatting.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| html | java.lang.String | An HTML string to insert into the document. |
| useBuilderFormatting | boolean | A value indicating whether formatting specified in [DocumentBuilder](../../com.aspose.words/documentbuilder/) is used as base formatting for text imported from HTML. |

### insertHtml(String html, int options) {#insertHtml-java.lang.String-int}
```
public void insertHtml(String html, int options)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| html | java.lang.String |  |
| options | int |  |

### insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark) {#insertHyperlink-java.lang.String-java.lang.String-boolean}
```
public Field insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark)
```


Inserts a hyperlink into the document.

 **Remarks:** 

Note that you need to specify font formatting for the hyperlink display text explicitly using the [getFont()](../../com.aspose.words/documentbuilder/\#getFont) property.

This methods internally calls [insertField(java.lang.String)](../../com.aspose.words/documentbuilder/\#insertField-java.lang.String) to insert an MS Word HYPERLINK field into the document.

 **Examples:** 

Shows how to insert a hyperlink which references a local bookmark.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startBookmark("Bookmark1");
 builder.write("Bookmarked text. ");
 builder.endBookmark("Bookmark1");
 builder.writeln("Text outside of the bookmark.");

 // Insert a HYPERLINK field that links to the bookmark. We can pass field switches
 // to the "InsertHyperlink" method as part of the argument containing the referenced bookmark's name.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 builder.insertHyperlink("Link to Bookmark1", "Bookmark1\" \\o \"Hyperlink Tip", true);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
 
```

Shows how to insert a hyperlink field.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("For more information, please visit the ");

 // Insert a hyperlink and emphasize it with custom formatting.
 // The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 builder.insertHyperlink("Google website", "https://www.google.com", false);
 builder.getFont().clearFormatting();
 builder.writeln(".");

 // Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlink.docx");
 
```

Shows how to use a document builder's formatting stack.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set up font formatting, then write the text that goes before the hyperlink.
 builder.getFont().setName("Arial");
 builder.getFont().setSize(24.0);
 builder.write("To visit Google, hold Ctrl and click ");

 // Preserve our current formatting configuration on the stack.
 builder.pushFont();

 // Alter the builder's current formatting by applying a new style.
 builder.getFont().setStyleIdentifier(StyleIdentifier.HYPERLINK);
 builder.insertHyperlink("here", "http://www.google.com", false);

 Assert.assertEquals(Color.BLUE.getRGB(), builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.SINGLE, builder.getFont().getUnderline());

 // Restore the font formatting that we saved earlier and remove the element from the stack.
 builder.popFont();

 Assert.assertEquals(0, builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.NONE, builder.getFont().getUnderline());

 builder.write(". We hope you enjoyed the example.");

 doc.save(getArtifactsDir() + "DocumentBuilder.PushPopFont.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| displayText | java.lang.String | Text of the link to be displayed in the document. |
| urlOrBookmark | java.lang.String | Link destination. Can be a url or a name of a bookmark inside the document. This method always adds apostrophes at the beginning and end of the url. |
| isBookmark | boolean |  true  if the previous parameter is a name of a bookmark inside the document;  false  is the previous parameter is a URL. |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the inserted field.
### insertImage(byte[] imageBytes) {#insertImage-byte}
```
public Shape insertImage(byte[] imageBytes)
```


Inserts an image from a byte array into the document. The image is inserted inline and at 100% scale.

 **Remarks:** 

You can change the image size, location, positioning method and other settings using the [Shape](../../com.aspose.words/shape/) object returned by this method.

 **Examples:** 

Shows how to insert an image from a byte array into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 byte[] imageByteArray = DocumentHelper.getBytesFromStream(new FileInputStream(getImageDir() + "Logo.jpg"));

 // Below are three ways of inserting an image from a byte array.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(imageByteArray);

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(imageByteArray, ConvertUtil.pixelToPoint(250.0), ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(imageByteArray, RelativeHorizontalPosition.MARGIN, 100.0, RelativeVerticalPosition.MARGIN,
         100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromByteArray.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | byte[] | The byte array that contains the image. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(byte[] imageBytes, double width, double height) {#insertImage-byte---double-double}
```
public Shape insertImage(byte[] imageBytes, double width, double height)
```


Inserts an inline image from a byte array into the document and scales it to the specified size.

 **Remarks:** 

You can change the image size, location, positioning method and other settings using the [Shape](../../com.aspose.words/shape/) object returned by this method.

 **Examples:** 

Shows how to insert an image from a byte array into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 byte[] imageByteArray = DocumentHelper.getBytesFromStream(new FileInputStream(getImageDir() + "Logo.jpg"));

 // Below are three ways of inserting an image from a byte array.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(imageByteArray);

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(imageByteArray, ConvertUtil.pixelToPoint(250.0), ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(imageByteArray, RelativeHorizontalPosition.MARGIN, 100.0, RelativeVerticalPosition.MARGIN,
         100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromByteArray.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | byte[] | The byte array that contains the image. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(byte[] imageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-byte---int-double-int-double-double-double-int}
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
[Shape](../../com.aspose.words/shape/)
### insertImage(BufferedImage image) {#insertImage-java.awt.image.BufferedImage}
```
public Shape insertImage(BufferedImage image)
```


Inserts an image into the document.  Inserts an image from a  object into the document. The image is inserted inline and at 100% scale.

 **Remarks:** 

You can change the image size, location, positioning method and other settings using the [Shape](../../com.aspose.words/shape/) object returned by this method.

Aspose.Words will insert the image in the PNG format and with default settings. If you want to insert a  BufferedImage  in another format or with other settings, you need to save the image into a byte array and use [insertImage(byte[])](../../com.aspose.words/documentbuilder/\#insertImage-byte).

 **Examples:** 

Shows how to insert an image from an object into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BufferedImage image = ImageIO.read(new File(getImageDir() + "Logo.jpg"));

 // Below are three ways of inserting an image from an Image object instance.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(image);

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(image, ConvertUtil.pixelToPoint(250.0), ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(image, RelativeHorizontalPosition.MARGIN, 100.0, RelativeVerticalPosition.MARGIN,
         100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromImageObject.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | The image to insert into the document. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(BufferedImage image, double width, double height) {#insertImage-java.awt.image.BufferedImage-double-double}
```
public Shape insertImage(BufferedImage image, double width, double height)
```


Inserts an inline image from a  object into the document and scales it to the specified size.

 **Remarks:** 

You can change the image size, location, positioning method and other settings using the [Shape](../../com.aspose.words/shape/) object returned by this method.

Aspose.Words will insert the image in the PNG format and with default settings. If you want to insert a  BufferedImage  in another format or with other settings, you need to save the image into a byte array and use [insertImage(byte[])](../../com.aspose.words/documentbuilder/\#insertImage-byte).

 **Examples:** 

Shows how to insert an image from an object into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BufferedImage image = ImageIO.read(new File(getImageDir() + "Logo.jpg"));

 // Below are three ways of inserting an image from an Image object instance.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(image);

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(image, ConvertUtil.pixelToPoint(250.0), ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(image, RelativeHorizontalPosition.MARGIN, 100.0, RelativeVerticalPosition.MARGIN,
         100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromImageObject.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | The image to insert into the document. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(BufferedImage image, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.awt.image.BufferedImage-int-double-int-double-double-double-int}
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
[Shape](../../com.aspose.words/shape/)
### insertImage(InputStream stream) {#insertImage-java.io.InputStream}
```
public Shape insertImage(InputStream stream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertImage(InputStream stream, double width, double height) {#insertImage-java.io.InputStream-double-double}
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
[Shape](../../com.aspose.words/shape/)
### insertImage(InputStream stream, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.io.InputStream-int-double-int-double-double-double-int}
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
[Shape](../../com.aspose.words/shape/)
### insertImage(String fileName) {#insertImage-java.lang.String}
```
public Shape insertImage(String fileName)
```


Inserts an image from a file or URL into the document. The image is inserted inline and at 100% scale.

 **Remarks:** 

This overload will automatically download the image before inserting into the document if you specify a remote URI.

You can change the image size, location, positioning method and other settings using the [Shape](../../com.aspose.words/shape/) object returned by this method.

 **Examples:** 

Shows how to insert gif image to the document.

```

 DocumentBuilder builder = new DocumentBuilder();

 // We can insert gif image using path or bytes array.
 // It works only if DocumentBuilder optimized to Word version 2010 or higher.
 // Note, that access to the image bytes causes conversion Gif to Png.
 Shape gifImage = builder.insertImage(getImageDir() + "Graphics Interchange Format.gif");

 gifImage = builder.insertImage(DocumentHelper.getBytesFromStream(new FileInputStream(getImageDir() + "Graphics Interchange Format.gif")));

 builder.getDocument().save(getArtifactsDir() + "InsertGif.docx");
 
```

Shows how to insert a shape with an image into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two locations where the document builder's "InsertShape" method
 // can source the image that the shape will display.
 // 1 -  Pass a local file system filename of an image file:
 builder.write("Image from local file: ");
 builder.insertImage(getImageDir() + "Logo.jpg");
 builder.writeln();

 // 2 -  Pass a URL which points to an image.
 builder.write("Image from a URL: ");
 builder.insertImage(getAsposelogoUri().toURL().openStream());
 builder.writeln();

 doc.save(getArtifactsDir() + "Image.FromUrl.docx");
 
```

Shows how to insert a floating image to the center of a page.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```

Shows how to determine which image will be inserted.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertImage(getImageDir() + "Scalable Vector Graphics.svg");

 // Aspose.Words insert SVG image to the document as PNG with svgBlip extension
 // that contains the original vector SVG image representation.
 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

 // Aspose.Words insert SVG image to the document as PNG, just like Microsoft Word does for old format.
 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertSvgImage.Svg.doc");

 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2003);

 // Aspose.Words insert SVG image to the document as EMF metafile to keep the image in vector representation.
 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertSvgImage.Emf.docx");
 
```

Shows how to insert an image from the local file system into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are three ways of inserting an image from a local system filename.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(getImageDir() + "Logo.jpg");

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(getImageDir() + "Transparent background logo.png", ConvertUtil.pixelToPoint(250.0),
         ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(getImageDir() + "Windows MetaFile.wmf", RelativeHorizontalPosition.MARGIN, 100.0,
         RelativeVerticalPosition.MARGIN, 100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromFilename.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The file with the image. Can be any valid local or remote URI. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(String fileName, double width, double height) {#insertImage-java.lang.String-double-double}
```
public Shape insertImage(String fileName, double width, double height)
```


Inserts an inline image from a file or URL into the document and scales it to the specified size.

 **Remarks:** 

You can change the image size, location, positioning method and other settings using the [Shape](../../com.aspose.words/shape/) object returned by this method.

 **Examples:** 

Shows how to insert an image from the local file system into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are three ways of inserting an image from a local system filename.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(getImageDir() + "Logo.jpg");

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(getImageDir() + "Transparent background logo.png", ConvertUtil.pixelToPoint(250.0),
         ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(getImageDir() + "Windows MetaFile.wmf", RelativeHorizontalPosition.MARGIN, 100.0,
         RelativeVerticalPosition.MARGIN, 100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromFilename.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The file that contains the image. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(String fileName, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.lang.String-int-double-int-double-double-double-int}
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
[Shape](../../com.aspose.words/shape/)
### insertNode(Node node) {#insertNode-com.aspose.words.Node}
```
public void insertNode(Node node)
```


Inserts a node before the cursor.

 **Examples:** 

Shows how to insert a linked image into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 String imageFileName = getImageDir() + "Windows MetaFile.wmf";

 // Below are two ways of applying an image to a shape so that it can display it.
 // 1 -  Set the shape to contain the image.
 Shape shape = new Shape(builder.getDocument(), ShapeType.IMAGE);
 shape.setWrapType(WrapType.INLINE);
 shape.getImageData().setImage(imageFileName);

 builder.insertNode(shape);

 doc.save(getArtifactsDir() + "Image.CreateLinkedImage.Embedded.docx");

 // Every image that we store in shape will increase the size of our document.
 Assert.assertTrue(new File(getArtifactsDir() + "Image.CreateLinkedImage.Embedded.docx").length() > 70000);

 doc.getFirstSection().getBody().getFirstParagraph().removeAllChildren();

 // 2 -  Set the shape to link to an image file in the local file system.
 shape = new Shape(builder.getDocument(), ShapeType.IMAGE);
 shape.setWrapType(WrapType.INLINE);
 shape.getImageData().setSourceFullName(imageFileName);

 builder.insertNode(shape);
 doc.save(getArtifactsDir() + "Image.CreateLinkedImage.Linked.docx");

 // Linking to images will save space and result in a smaller document.
 // However, the document can only display the image correctly while
 // the image file is present at the location that the shape's "SourceFullName" property points to.
 Assert.assertTrue(new File(getArtifactsDir() + "Image.CreateLinkedImage.Linked.docx").length() < 10000);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) |  |

### insertOleObject(InputStream stream, String progId, boolean asIcon, InputStream presentation) {#insertOleObject-java.io.InputStream-java.lang.String-boolean-java.io.InputStream}
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
[Shape](../../com.aspose.words/shape/)
### insertOleObject(String fileName, boolean isLinked, boolean asIcon, InputStream presentation) {#insertOleObject-java.lang.String-boolean-boolean-java.io.InputStream}
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
[Shape](../../com.aspose.words/shape/)
### insertOleObject(String fileName, String progId, boolean isLinked, boolean asIcon, InputStream presentation) {#insertOleObject-java.lang.String-java.lang.String-boolean-boolean-java.io.InputStream}
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
[Shape](../../com.aspose.words/shape/)
### insertOleObjectAsIcon(InputStream stream, String progId, String iconFile, String iconCaption) {#insertOleObjectAsIcon-java.io.InputStream-java.lang.String-java.lang.String-java.lang.String}
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
[Shape](../../com.aspose.words/shape/)
### insertOleObjectAsIcon(String fileName, boolean isLinked, String iconFile, String iconCaption) {#insertOleObjectAsIcon-java.lang.String-boolean-java.lang.String-java.lang.String}
```
public Shape insertOleObjectAsIcon(String fileName, boolean isLinked, String iconFile, String iconCaption)
```


Inserts an embedded or linked OLE object as icon into the document. Allows to specify icon file and caption. Detects OLE object type using file extension.

 **Examples:** 

Shows how to insert an OLE object into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // OLE objects are links to files in our local file system that can be opened by other installed applications.
 // Double clicking these shapes will launch the application, and then use it to open the linked object.
 // There are three ways of using the InsertOleObject method to insert these shapes and configure their appearance.
 // If 'presentation' is omitted and 'asIcon' is set, this overloaded method selects
 // the icon according to the file extension and uses the filename for the icon caption.
 // 1 -  Image taken from the local file system:
 builder.insertOleObject(getMyDir() + "Spreadsheet.xlsx", false, false, new FileInputStream(getImageDir() + "Logo.jpg"));

 // If 'presentation' is omitted and 'asIcon' is set, this overloaded method selects
 // the icon according to 'progId' and uses the filename for the icon caption.
 // 2 -  Icon based on the application that will open the object:
 builder.insertOleObject(getMyDir() + "Spreadsheet.xlsx", "Excel.Sheet", false, true, new FileInputStream(getImageDir() + "Logo.jpg"));

 // If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
 // the icon according to 'progId' and uses the predefined icon caption.
 // 3 -  Image icon that's 32 x 32 pixels or smaller from the local file system, with a custom caption:
 builder.insertOleObjectAsIcon(getMyDir() + "Presentation.pptx", false, getImageDir() + "Logo icon.ico",
         "Double click to view presentation!");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertOleObject.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Full path to the file. |
| isLinked | boolean | If  true  then linked OLE object is inserted otherwise embedded OLE object is inserted. |
| iconFile | java.lang.String | Full path to the ICO file. If the value is  null , Aspose.Words will use a predefined image. |
| iconCaption | java.lang.String | Icon caption. If the value is  null , Aspose.Words will use the file name. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - Shape node containing Ole object and inserted at the current Builder position.
### insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption) {#insertOleObjectAsIcon-java.lang.String-java.lang.String-boolean-java.lang.String-java.lang.String}
```
public Shape insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption)
```


Inserts an embedded or linked OLE object as icon into the document. Allows to specify icon file and caption. Detects OLE object type using given progID parameter.

 **Examples:** 

Shows how to insert an embedded or linked OLE object as icon into the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
 // the icon according to 'progId' and uses the filename for the icon caption.
 builder.insertOleObjectAsIcon(getMyDir() + "Presentation.pptx", "Package", false, getImageDir() + "Logo icon.ico", "My embedded file");

 builder.insertBreak(BreakType.LINE_BREAK);

 try (FileInputStream stream = new FileInputStream(getMyDir() + "Presentation.pptx")) {
     // If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
     // the icon according to the file extension and uses the filename for the icon caption.
     Shape shape = builder.insertOleObjectAsIcon(stream, "PowerPoint.Application", getImageDir() + "Logo icon.ico",
             "My embedded file stream");

     OlePackage setOlePackage = shape.getOleFormat().getOlePackage();
     setOlePackage.setFileName("Presentation.pptx");
     setOlePackage.setDisplayName("Presentation.pptx");
 }

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertOleObjectAsIcon.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Full path to the file. |
| progId | java.lang.String | ProgId of OLE object. |
| isLinked | boolean | If  true  then linked OLE object is inserted otherwise embedded OLE object is inserted. |
| iconFile | java.lang.String | Full path to the ICO file. If the value is  null , Aspose.Words will use a predefined image. |
| iconCaption | java.lang.String | Icon caption. If the value is  null , Aspose.Words will use the file name. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - Shape node containing Ole object and inserted at the current Builder position.
### insertOnlineVideo(String videoUrl, double width, double height) {#insertOnlineVideo-java.lang.String-double-double}
```
public Shape insertOnlineVideo(String videoUrl, double width, double height)
```


Inserts an online video object into the document and scales it to the specified size.

 **Remarks:** 

You can change the image size, location, positioning method and other settings using the [Shape](../../com.aspose.words/shape/) object returned by this method.

Insertion of online video from the following resources is supported:

 *  https://www.youtube.com/
 *  https://vimeo.com/

If your online video is not displaying correctly, use [insertOnlineVideo(java.lang.String, java.lang.String, byte[], double, double)](../../com.aspose.words/documentbuilder/\#insertOnlineVideo-java.lang.String--java.lang.String--byte----double--double), which accepts custom embedded html code.

The code for embedding video can vary between providers, consult your corresponding provider of choice for details.

 **Examples:** 

Shows how to insert an online video into a document using a URL.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertOnlineVideo("https://youtu.be/t_1LYZ102RA", 360.0, 270.0);

 // We can watch the video from Microsoft Word by clicking on the shape.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertVideoWithUrl.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| videoUrl | java.lang.String | The URL to the video. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertOnlineVideo(String videoUrl, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertOnlineVideo-java.lang.String-int-double-int-double-double-double-int}
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
[Shape](../../com.aspose.words/shape/)
### insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height) {#insertOnlineVideo-java.lang.String-java.lang.String-byte---double-double}
```
public Shape insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height)
```


Inserts an online video object into the document and scales it to the specified size.

 **Remarks:** 

You can change the image size, location, positioning method and other settings using the [Shape](../../com.aspose.words/shape/) object returned by this method.

 **Examples:** 

Shows how to insert an online video into a document with a custom thumbnail.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 String videoUrl = "https://vimeo.com/52477838";
 String videoEmbedCode = "";

 byte[] thumbnailImageBytes = IOUtils.toByteArray(getAsposelogoUri().toURL().openStream());

 BufferedImage image = ImageIO.read(new ByteArrayInputStream(thumbnailImageBytes));

 // Below are two ways of creating a shape with a custom thumbnail, which links to an online video
 // that will play when we click on the shape in Microsoft Word.
 // 1 -  Insert an inline shape at the builder's node insertion cursor:
 builder.insertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.getWidth(), image.getHeight());

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Insert a floating shape:
 double left = builder.getPageSetup().getRightMargin() - image.getWidth();
 double top = builder.getPageSetup().getBottomMargin() - image.getHeight();

 builder.insertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
         RelativeHorizontalPosition.RIGHT_MARGIN, left, RelativeVerticalPosition.BOTTOM_MARGIN, top,
         image.getWidth(), image.getHeight(), WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| videoUrl | java.lang.String | The URL to the video. |
| videoEmbedCode | java.lang.String | The embed code for the video. |
| thumbnailImageBytes | byte[] | The thumbnail image bytes. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertOnlineVideo-java.lang.String-java.lang.String-byte---int-double-int-double-double-double-int}
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
[Shape](../../com.aspose.words/shape/)
### insertParagraph() {#insertParagraph}
```
public Paragraph insertParagraph()
```


Inserts a paragraph break into the document.

 **Remarks:** 

Current paragraph formatting specified by the [getParagraphFormat()](../../com.aspose.words/documentbuilder/\#getParagraphFormat) property is used.

Breaks the current paragraph in two. After inserting the paragraph, the cursor is placed at the beginning of the new paragraph.

An exception is thrown if it is not possible to insert a paragraph break at the current cursor position.

 **Examples:** 

Shows how to insert a paragraph into the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
```

**Returns:**
[Paragraph](../../com.aspose.words/paragraph/) - The paragraph node that was just inserted. It is the same node as [getCurrentParagraph()](../../com.aspose.words/documentbuilder/\#getCurrentParagraph).
### insertShape(int shapeType, double width, double height) {#insertShape-int-double-double}
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
[Shape](../../com.aspose.words/shape/)
### insertShape(int shapeType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertShape-int-int-double-int-double-double-double-int}
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
[Shape](../../com.aspose.words/shape/)
### insertSignatureLine(SignatureLineOptions signatureLineOptions) {#insertSignatureLine-com.aspose.words.SignatureLineOptions}
```
public Shape insertSignatureLine(SignatureLineOptions signatureLineOptions)
```


Inserts a signature line at the current position.

 **Examples:** 

Shows how to sign a document with a personal certificate and a signature line.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions signatureLineOptions = new SignatureLineOptions();
 signatureLineOptions.setSigner("vderyushev");
 signatureLineOptions.setSignerTitle("QA");
 signatureLineOptions.setEmail("vderyushev@aspose.com");
 signatureLineOptions.setShowDate(true);
 signatureLineOptions.setDefaultInstructions(false);
 signatureLineOptions.setInstructions("Please sign here.");
 signatureLineOptions.setAllowComments(true);

 SignatureLine signatureLine = builder.insertSignatureLine(signatureLineOptions).getSignatureLine();
 signatureLine.setProviderId(UUID.fromString("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2"));

 Assert.assertFalse(signatureLine.isSigned());
 Assert.assertFalse(signatureLine.isValid());

 doc.save(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.docx");

 Date currentDate = new Date();

 SignOptions signOptions = new SignOptions();
 signOptions.setSignatureLineId(signatureLine.getId());
 signOptions.setProviderId(signatureLine.getProviderId());
 signOptions.setComments("Document was signed by vderyushev");
 signOptions.setSignTime(currentDate);

 CertificateHolder certHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 DigitalSignatureUtil.sign(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.docx",
         getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

 // Re-open our saved document, and verify that the "IsSigned" and "IsValid" properties both equal "true",
 // indicating that the signature line contains a signature.
 doc = new Document(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 signatureLine = shape.getSignatureLine();

 Assert.assertTrue(signatureLine.isSigned());
 Assert.assertTrue(signatureLine.isValid());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| signatureLineOptions | [SignatureLineOptions](../../com.aspose.words/signaturelineoptions/) | The object that stores parameters of creating signature line. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The signature line node that was just inserted.
### insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType) {#insertSignatureLine-com.aspose.words.SignatureLineOptions-int-double-int-double-int}
```
public Shape insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| signatureLineOptions | [SignatureLineOptions](../../com.aspose.words/signaturelineoptions/) |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertStyleSeparator() {#insertStyleSeparator}
```
public void insertStyleSeparator()
```


Inserts style separator into the document.

 **Remarks:** 

This method allows to apply different paragraph styles to two different parts of a text line.

 **Examples:** 

Shows how to work with style separators.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Each paragraph can only have one style.
 // The InsertStyleSeparator method allows us to work around this limitation.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.write("This text is in a Heading style. ");
 builder.insertStyleSeparator();

 Style paraStyle = builder.getDocument().getStyles().add(StyleType.PARAGRAPH, "MyParaStyle");
 paraStyle.getFont().setBold(false);
 paraStyle.getFont().setSize(8.0);
 paraStyle.getFont().setName("Arial");

 builder.getParagraphFormat().setStyleName(paraStyle.getName());
 builder.write("This text is in a custom style. ");

 // Calling the InsertStyleSeparator method creates another paragraph,
 // which can have a different style to the previous. There will be no break between paragraphs.
 // The text in the output document will look like one paragraph with two styles.
 Assert.assertEquals(2, doc.getFirstSection().getBody().getParagraphs().getCount());
 Assert.assertEquals("Heading 1", doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle().getName());
 Assert.assertEquals("MyParaStyle", doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle().getName());

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertStyleSeparator.docx");
 
```

### insertTableOfContents(String switches) {#insertTableOfContents-java.lang.String}
```
public Field insertTableOfContents(String switches)
```


Inserts a TOC (table of contents) field into the document.

 **Remarks:** 

This method inserts a TOC (table of contents) field into the document at the current position.

A table of contents in a Word document can be built in a number of ways and formatted using a variety of options. The way the table is built and displayed by Microsoft Word is controlled by the field switches.

The easiest way to specify the switches is to insert and configure a table of contents into a Word document using the Insert->Reference->Index and Tables menu, then switch display of field codes on to see the switches. You can press Alt+F9 in Microsoft Word to toggle display of field codes on or off.

For example, after creating a table of contents, the following field is inserted into the document: **\{ TOC \\o "1-3" \\h \\z \}**. You can copy **\\o "1-3" \\h \\z**  and use it as the switches parameter.

Note that [insertTableOfContents(java.lang.String)](../../com.aspose.words/documentbuilder/\#insertTableOfContents-java.lang.String) will only insert a TOC field, but will not actually build the table of contents. The table of contents is built by Microsoft Word when the field is updated.

If you insert a table of contents using this method and then open the file in Microsoft Word, you will not see the table of contents because the TOC field has not yet been updated.

In Microsoft Word, fields are not automatically updated when a document is opened, but you can update fields in a document at any time by pressing F9.

 **Examples:** 

Shows how to insert a Table of contents (TOC) into a document using heading styles as entries.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a table of contents for the first page of the document.
 // Configure the table to pick up paragraphs with headings of levels 1 to 3.
 // Also, set its entries to be hyperlinks that will take us
 // to the location of the heading when left-clicked in Microsoft Word.
 builder.insertTableOfContents("\\o \"1-3\" \\h \\z \\u");
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Populate the table of contents by adding paragraphs with heading styles.
 // Each such heading with a level between 1 and 3 will create an entry in the table.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 2");
 builder.writeln("Heading 3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);
 builder.writeln("Heading 3.1.1");
 builder.writeln("Heading 3.1.2");
 builder.writeln("Heading 3.1.3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_4);
 builder.writeln("Heading 3.1.3.1");
 builder.writeln("Heading 3.1.3.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.2");
 builder.writeln("Heading 3.3");

 // A table of contents is a field of a type that needs to be updated to show an up-to-date result.
 doc.updateFields();
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertToc.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| switches | java.lang.String | The TOC field switches. |

**Returns:**
[Field](../../com.aspose.words/field/)
### insertTextInput(String name, int type, String format, String fieldValue, int maxLength) {#insertTextInput-java.lang.String-int-java.lang.String-java.lang.String-int}
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
[FormField](../../com.aspose.words/formfield/)
### isAtEndOfParagraph() {#isAtEndOfParagraph}
```
public boolean isAtEndOfParagraph()
```


Returns  true  if the cursor is at the end of the current paragraph.

 **Examples:** 

Shows how to move a document builder's cursor to different nodes in a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

**Returns:**
boolean -  true  if the cursor is at the end of the current paragraph.
### isAtEndOfStructuredDocumentTag() {#isAtEndOfStructuredDocumentTag}
```
public boolean isAtEndOfStructuredDocumentTag()
```


Returns **true** if the cursor is at the end of a structured document tag.

 **Examples:** 

Shows how to move cursor of DocumentBuilder inside a structured document tag.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 // There is a several ways to move the cursor:
 // 1 -  Move to the first character of structured document tag by index.
 builder.moveToStructuredDocumentTag(1, 1);

 // 2 -  Move to the first character of structured document tag by object.
 StructuredDocumentTag tag = (StructuredDocumentTag)doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG, 2, true);
 builder.moveToStructuredDocumentTag(tag, 1);
 builder.write(" New text.");

 Assert.assertEquals("R New text.ichText", tag.getText().trim());

 // 3 -  Move to the end of the second structured document tag.
 builder.moveToStructuredDocumentTag(1, -1);
 Assert.assertTrue(builder.isAtEndOfStructuredDocumentTag());

 // Get currently selected structured document tag.
 builder.getCurrentStructuredDocumentTag().setColor(Color.GREEN);

 doc.save(getArtifactsDir() + "Document.MoveToStructuredDocumentTag.docx");
 
```

**Returns:**
boolean - **true** if the cursor is at the end of a structured document tag.
### isAtStartOfParagraph() {#isAtStartOfParagraph}
```
public boolean isAtStartOfParagraph()
```


Returns  true  if the cursor is at the beginning of the current paragraph (no text before the cursor).

 **Examples:** 

Shows how to move a document builder's cursor to different nodes in a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

**Returns:**
boolean -  true  if the cursor is at the beginning of the current paragraph (no text before the cursor).
### moveTo(Node node) {#moveTo-com.aspose.words.Node}
```
public void moveTo(Node node)
```


Moves the cursor to an inline node or to the end of a paragraph.

 **Remarks:** 

When *node* is an inline-level node, the cursor is moved to this node and further content will be inserted before that node.

When *node* is a [Paragraph](../../com.aspose.words/paragraph/), the cursor is moved to the end of the paragraph and further content will be inserted just before the paragraph break.

When *node* is a block-level node but not a [Paragraph](../../com.aspose.words/paragraph/), the cursor is moved to the end of the first paragraph into block-level node and further content will be inserted just before the paragraph break.

 **Examples:** 

Shows how to move a DocumentBuilder's cursor position to a specified node.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Run 1. ");

 // The document builder has a cursor, which acts as the part of the document
 // where the builder appends new nodes when we use its document construction methods.
 // This cursor functions in the same way as Microsoft Word's blinking cursor,
 // and it also always ends up immediately after any node that the builder just inserted.
 // To append content to a different part of the document,
 // we can move the cursor to a different node with the "MoveTo" method.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0));
 // The cursor is now in front of the node that we moved it to.
 // Adding a second run will insert it in front of the first run.
 builder.writeln("Run 2. ");

 Assert.assertEquals("Run 2. \rRun 1.", doc.getText().trim());

 // Move the cursor to the end of the document to continue appending text to the end as before.
 builder.moveTo(doc.getLastSection().getBody().getLastParagraph());
 builder.writeln("Run 3. ");

 Assert.assertEquals("Run 2. \rRun 1. \rRun 3.", doc.getText().trim());
 
```

Shows how to move a document builder's cursor to different nodes in a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | The node must be a paragraph or a direct child of a paragraph. |

### moveToBookmark(String bookmarkName) {#moveToBookmark-java.lang.String}
```
public boolean moveToBookmark(String bookmarkName)
```


Moves the cursor to a bookmark.

 **Remarks:** 

Moves the cursor to a position just after the start of the bookmark with the specified name.

The comparison is not case-sensitive. If the bookmark was not found,  false  is returned and the cursor is not moved.

Inserting new text does not replace existing text of the bookmark.

Note that some bookmarks in the document are assigned to form fields. Moving to such a bookmark and inserting text there inserts the text into the form field code. Although this will not invalidate the form field, the inserted text will not be visible because it becomes part of the field code.

 **Examples:** 

Shows how to move a document builder's cursor to different nodes in a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | The name of the bookmark to move the cursor to. |

**Returns:**
boolean -  true  if the bookmark was found;  false  otherwise.
### moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter) {#moveToBookmark-java.lang.String-boolean-boolean}
```
public boolean moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter)
```


Moves the cursor to a bookmark with greater precision.

 **Remarks:** 

Moves the cursor to a position before or after the bookmark start or end.

If desired position is not at inline level, moves to the next paragraph.

The comparison is not case-sensitive. If the bookmark was not found,  false  is returned and the cursor is not moved.

 **Examples:** 

Shows how to move a document builder's node insertion point cursor to a bookmark.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A valid bookmark consists of a BookmarkStart node, a BookmarkEnd node with a
 // matching bookmark name somewhere afterward, and contents enclosed by those nodes.
 builder.startBookmark("MyBookmark");
 builder.write("Hello world! ");
 builder.endBookmark("MyBookmark");

 // There are 4 ways of moving a document builder's cursor to a bookmark.
 // If we are between the BookmarkStart and BookmarkEnd nodes, the cursor will be inside the bookmark.
 // This means that any text added by the builder will become a part of the bookmark.
 // 1 -  Outside of the bookmark, in front of the BookmarkStart node:
 Assert.assertTrue(builder.moveToBookmark("MyBookmark", true, false));
 builder.write("1. ");

 Assert.assertEquals("Hello world! ", doc.getRange().getBookmarks().get("MyBookmark").getText());
 Assert.assertEquals("1. Hello world!", doc.getText().trim());

 // 2 -  Inside the bookmark, right after the BookmarkStart node:
 Assert.assertTrue(builder.moveToBookmark("MyBookmark", true, true));
 builder.write("2. ");

 Assert.assertEquals("2. Hello world! ", doc.getRange().getBookmarks().get("MyBookmark").getText());
 Assert.assertEquals("1. 2. Hello world!", doc.getText().trim());

 // 2 -  Inside the bookmark, right in front of the BookmarkEnd node:
 Assert.assertTrue(builder.moveToBookmark("MyBookmark", false, false));
 builder.write("3. ");

 Assert.assertEquals("2. Hello world! 3. ", doc.getRange().getBookmarks().get("MyBookmark").getText());
 Assert.assertEquals("1. 2. Hello world! 3.", doc.getText().trim());

 // 4 -  Outside of the bookmark, after the BookmarkEnd node:
 Assert.assertTrue(builder.moveToBookmark("MyBookmark", false, true));
 builder.write("4.");

 Assert.assertEquals("2. Hello world! 3. ", doc.getRange().getBookmarks().get("MyBookmark").getText());
 Assert.assertEquals("1. 2. Hello world! 3. 4.", doc.getText().trim());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | The name of the bookmark to move the cursor to. |
| isStart | boolean | When  true , moves the cursor to the beginning of the bookmark. When  false , moves the cursor to the end of the bookmark. |
| isAfter | boolean | When  true , moves the cursor to be after the bookmark start or end position. When  false , moves the cursor to be before the bookmark start or end position. |

**Returns:**
boolean -  true  if the bookmark was found;  false  otherwise.
### moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex) {#moveToCell-int-int-int-int}
```
public void moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)
```


Moves the cursor to a table cell in the current section.

 **Remarks:** 

The navigation is performed inside the current story of the current section.

For the index parameters, when index is greater than or equal to 0, it specifies an index from the beginning with 0 being the first element. When index is less than 0, it specified an index from the end with -1 being the last element.

 **Examples:** 

Shows how to move a document builder's cursor to a cell in a table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an empty 2x2 table.
 builder.startTable();
 builder.insertCell();
 builder.insertCell();
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 // Because we have ended the table with the EndTable method,
 // the document builder's cursor is currently outside the table.
 // This cursor has the same function as Microsoft Word's blinking text cursor.
 // It can also be moved to a different location in the document using the builder's MoveTo methods.
 // We can move the cursor back inside the table to a specific cell.
 builder.moveToCell(0, 1, 1, 0);
 builder.write("Column 2, cell 2.");

 doc.save(getArtifactsDir() + "DocumentBuilder.MoveToCell.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tableIndex | int | The index of the table to move to. |
| rowIndex | int | The index of the row in the table. |
| columnIndex | int | The index of the column in the table. |
| characterIndex | int | The index of the character inside the cell. A negative value allows you to specify a position from the end of the cell. Use -1 to move to the end of the cell. |

### moveToDocumentEnd() {#moveToDocumentEnd}
```
public void moveToDocumentEnd()
```


Moves the cursor to the end of the document.

 **Examples:** 

Shows how to move a document builder's cursor to different nodes in a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

### moveToDocumentStart() {#moveToDocumentStart}
```
public void moveToDocumentStart()
```


Moves the cursor to the beginning of the document.

 **Examples:** 

Shows how to move a document builder's cursor to different nodes in a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

### moveToField(Field field, boolean isAfter) {#moveToField-com.aspose.words.Field-boolean}
```
public void moveToField(Field field, boolean isAfter)
```


Moves the cursor to a field in the document.

 **Examples:** 

Shows how to move a document builder's node insertion point cursor to a specific field.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a field using the DocumentBuilder and add a run of text after it.
 Field field = builder.insertField(" AUTHOR \"John Doe\" ");

 // The builder's cursor is currently at end of the document.
 Assert.assertNull(builder.getCurrentNode());

 // Move the cursor to the field while specifying whether to place that cursor before or after the field.
 builder.moveToField(field, moveCursorToAfterTheField);

 // Note that the cursor is outside of the field in both cases.
 // This means that we cannot edit the field using the builder like this.
 // To edit a field, we can use the builder's MoveTo method on a field's FieldStart
 // or FieldSeparator node to place the cursor inside.
 if (moveCursorToAfterTheField) {
     Assert.assertNull(builder.getCurrentNode());
     builder.write(" Text immediately after the field.");

     Assert.assertEquals("AUTHOR \"John Doe\" John Doe Text immediately after the field.",
             doc.getText().trim());
 } else {
     Assert.assertEquals(field.getStart(), builder.getCurrentNode());
     builder.write("Text immediately before the field. ");

     Assert.assertEquals("Text immediately before the field.  AUTHOR \"John Doe\" John Doe",
             doc.getText().trim());
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| field | [Field](../../com.aspose.words/field/) | The field to move the cursor to. |
| isAfter | boolean | When  true , moves the cursor to be after the field end. When  false , moves the cursor to be before the field start. |

### moveToHeaderFooter(int headerFooterType) {#moveToHeaderFooter-int}
```
public void moveToHeaderFooter(int headerFooterType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| headerFooterType | int |  |

### moveToMergeField(String fieldName) {#moveToMergeField-java.lang.String}
```
public boolean moveToMergeField(String fieldName)
```


Moves the cursor to the specified merge field.  Moves the cursor to a position just beyond the specified merge field and removes the merge field.

 **Remarks:** 

Note that this method deletes the merge field from the document after moving the cursor.

 **Examples:** 

Shows how to fill MERGEFIELDs with data with a document builder instead of a mail merge.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
 // and then fill them manually.
 builder.insertField(" MERGEFIELD Chairman ");
 builder.insertField(" MERGEFIELD ChiefFinancialOfficer ");
 builder.insertField(" MERGEFIELD ChiefTechnologyOfficer ");

 builder.moveToMergeField("Chairman");
 builder.setBold(true);
 builder.writeln("John Doe");

 builder.moveToMergeField("ChiefFinancialOfficer");
 builder.setItalic(true);
 builder.writeln("Jane Doe");

 builder.moveToMergeField("ChiefTechnologyOfficer");
 builder.setItalic(true);
 builder.writeln("John Bloggs");

 doc.save(getArtifactsDir() + "DocumentBuilder.FillMergeFields.docx");
 
```

Shows how to insert checkbox form fields into a document during mail merge.

```

 public void insertCheckBox() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startTable();
     builder.insertCell();
     builder.insertField(" MERGEFIELD  TableStart:StudentCourse ");
     builder.insertCell();
     builder.insertField(" MERGEFIELD  CourseName ");
     builder.insertCell();
     builder.insertField(" MERGEFIELD  TableEnd:StudentCourse ");
     builder.endTable();

     // Add a handler for the MergeField event
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeFieldInsertCheckBox());

     // Execute mail merge with regions
     DataTable dataTable = getStudentCourseDataTable();
     doc.getMailMerge().executeWithRegions(dataTable);

     // Save resulting document with a new name
     doc.save(getArtifactsDir() + "MailMergeEvent.InsertCheckBox.docx");
 }

 private class HandleMergeFieldInsertCheckBox implements IFieldMergingCallback {
     // This is called for each merge field in the document
     // when Document.MailMerge.ExecuteWithRegions is called.
     public void fieldMerging(final FieldMergingArgs args) throws Exception {
         if (args.getDocumentFieldName().equals("CourseName")) {
             // The name of the table that we are merging can be found here
             Assert.assertEquals(args.getTableName(), "StudentCourse");

             // Insert the checkbox for this merge field, using DocumentBuilder
             DocumentBuilder builder = new DocumentBuilder(args.getDocument());
             builder.moveToMergeField(args.getFieldName());
             builder.insertCheckBox(args.getDocumentFieldName() + mCheckBoxCount, false, 0);
             // Get the actual value of the field
             String fieldValue = args.getFieldValue().toString();

             // In this case, for every record index 'n', the corresponding field value is "Course n"
             Assert.assertEquals(args.getRecordIndex(), Character.getNumericValue(fieldValue.charAt(7)));

             builder.write(fieldValue);
             mCheckBoxCount++;
         }
     }

     public void imageFieldMerging(final ImageFieldMergingArgs args) {
         // Do nothing
     }

     // Counter for CheckBox name generation.
     private int mCheckBoxCount;
 }

 // Create DataTable and fill it with data.
 // In real life this DataTable should be filled from a database.
 private static DataTable getStudentCourseDataTable() throws Exception {
     DataTable dataTable = new DataTable("StudentCourse");
     dataTable.getColumns().add("CourseName");
     for (int i = 0; i < 10; i++) {
         DataRow datarow = dataTable.newRow();
         dataTable.getRows().add(datarow);
         datarow.set(0, "Course " + i);
     }
     return dataTable;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldName | java.lang.String | The case-insensitive name of the mail merge field. |

**Returns:**
boolean -  true  if the merge field was found and the cursor was moved;  false  otherwise.
### moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField) {#moveToMergeField-java.lang.String-boolean-boolean}
```
public boolean moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField)
```


Moves the merge field to the specified merge field.

 **Examples:** 

Shows how to insert fields, and move the document builder's cursor to them.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertField("MERGEFIELD MyMergeField1 \\* MERGEFORMAT");
 builder.insertField("MERGEFIELD MyMergeField2 \\* MERGEFORMAT");

 // Move the cursor to the first MERGEFIELD.
 builder.moveToMergeField("MyMergeField1", true, false);

 // Note that the cursor is placed immediately after the first MERGEFIELD, and before the second.
 Assert.assertEquals(doc.getRange().getFields().get(1).getStart(), builder.getCurrentNode());
 Assert.assertEquals(doc.getRange().getFields().get(0).getEnd(), builder.getCurrentNode().getPreviousSibling());

 // If we wish to edit the field's field code or contents using the builder,
 // its cursor would need to be inside a field.
 // To place it inside a field, we would need to call the document builder's MoveTo method
 // and pass the field's start or separator node as an argument.
 builder.write(" Text between our merge fields. ");

 doc.save(getArtifactsDir() + "DocumentBuilder.MergeFields.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldName | java.lang.String | The case-insensitive name of the mail merge field. |
| isAfter | boolean | When  true , moves the cursor to be after the field end. When  false , moves the cursor to be before the field start. |
| isDeleteField | boolean | When  true , deletes the merge field. |

**Returns:**
boolean -  true  if the merge field was found and the cursor was moved;  false  otherwise.
### moveToParagraph(int paragraphIndex, int characterIndex) {#moveToParagraph-int-int}
```
public void moveToParagraph(int paragraphIndex, int characterIndex)
```


Moves the cursor to a paragraph in the current section.

 **Remarks:** 

The navigation is performed inside the current story of the current section. That is, if you moved the cursor to the primary header of the first section, then  paragraphIndex  specified the index of the paragraph inside that header of that section.

When  paragraphIndex  is greater than or equal to 0, it specifies an index from the beginning of the section with 0 being the first paragraph. When  paragraphIndex  is less than 0, it specified an index from the end of the section with -1 being the last paragraph.

 **Examples:** 

Shows how to move a builder's cursor position to a specified paragraph.

```

 Document doc = new Document(getMyDir() + "Paragraphs.docx");
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(22, paragraphs.getCount());

 // Create document builder to edit the document. The builder's cursor,
 // which is the point where it will insert new nodes when we call its document construction methods,
 // is currently at the beginning of the document.
 DocumentBuilder builder = new DocumentBuilder(doc);

 Assert.assertEquals(0, paragraphs.indexOf(builder.getCurrentParagraph()));

 // Move that cursor to a different paragraph will place that cursor in front of that paragraph.
 builder.moveToParagraph(2, 0);
 // Any new content that we add will be inserted at that point.
 builder.writeln("This is a new third paragraph. ");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| paragraphIndex | int | The index of the paragraph to move to. |
| characterIndex | int | The index of the character inside the paragraph. A negative value allows you to specify a position from the end of the paragraph. Use -1 to move to the end of the paragraph. |

### moveToSection(int sectionIndex) {#moveToSection-int}
```
public void moveToSection(int sectionIndex)
```


Moves the cursor to the beginning of the body in a specified section.

 **Remarks:** 

When  sectionIndex  is greater than or equal to 0, it specifies an index from the beginning of the document with 0 being the first section. When  sectionIndex  is less than 0, it specified an index from the end of the document with -1 being the last section.

The cursor is moved to the first paragraph in the [Body](../../com.aspose.words/body/) of the specified section.

 **Examples:** 

Shows how to create headers and footers in a document using DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sectionIndex | int | The index of the section to move to. |

### moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex) {#moveToStructuredDocumentTag-com.aspose.words.StructuredDocumentTag-int}
```
public void moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex)
```


Moves the cursor to the structured document tag.

 **Examples:** 

Shows how to move cursor of DocumentBuilder inside a structured document tag.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 // There is a several ways to move the cursor:
 // 1 -  Move to the first character of structured document tag by index.
 builder.moveToStructuredDocumentTag(1, 1);

 // 2 -  Move to the first character of structured document tag by object.
 StructuredDocumentTag tag = (StructuredDocumentTag)doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG, 2, true);
 builder.moveToStructuredDocumentTag(tag, 1);
 builder.write(" New text.");

 Assert.assertEquals("R New text.ichText", tag.getText().trim());

 // 3 -  Move to the end of the second structured document tag.
 builder.moveToStructuredDocumentTag(1, -1);
 Assert.assertTrue(builder.isAtEndOfStructuredDocumentTag());

 // Get currently selected structured document tag.
 builder.getCurrentStructuredDocumentTag().setColor(Color.GREEN);

 doc.save(getArtifactsDir() + "Document.MoveToStructuredDocumentTag.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| structuredDocumentTag | [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) | The structured document tag to move to. |
| characterIndex | int | The index of the character inside the structured document tag. A negative value allows you to specify a position from the end of the structured document tag. Use -1 to move to the end of the structured document tag. If the structured document tag is at the block level, and you want to move the cursor to the end of its last paragraph, specify -2. |

### moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex) {#moveToStructuredDocumentTag-int-int}
```
public void moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```


Moves the cursor to a structured document tag in the current section.

 **Remarks:** 

The navigation is performed inside the current story of the current section. That is, if you moved the cursor to the primary header of the first section, then  structuredDocumentTagIndex  specified the index of the structured document tag inside that header of that section.

When  structuredDocumentTagIndex  is greater than or equal to 0, it specifies an index from the beginning of the section with 0 being the first structured document tag. When  structuredDocumentTagIndex  is less than 0, it specified an index from the end of the section with -1 being the last structured document tag.

 **Examples:** 

Shows how to move cursor of DocumentBuilder inside a structured document tag.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 // There is a several ways to move the cursor:
 // 1 -  Move to the first character of structured document tag by index.
 builder.moveToStructuredDocumentTag(1, 1);

 // 2 -  Move to the first character of structured document tag by object.
 StructuredDocumentTag tag = (StructuredDocumentTag)doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG, 2, true);
 builder.moveToStructuredDocumentTag(tag, 1);
 builder.write(" New text.");

 Assert.assertEquals("R New text.ichText", tag.getText().trim());

 // 3 -  Move to the end of the second structured document tag.
 builder.moveToStructuredDocumentTag(1, -1);
 Assert.assertTrue(builder.isAtEndOfStructuredDocumentTag());

 // Get currently selected structured document tag.
 builder.getCurrentStructuredDocumentTag().setColor(Color.GREEN);

 doc.save(getArtifactsDir() + "Document.MoveToStructuredDocumentTag.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| structuredDocumentTagIndex | int | The index of the structured document tag to move to. |
| characterIndex | int | The index of the character inside the structured document tag. A negative value allows you to specify a position from the end of the structured document tag. Use -1 to move to the end of the structured document tag. If the structured document tag is at the block level, and you want to move the cursor to the end of its last paragraph, specify -2. |

### popFont() {#popFont}
```
public void popFont()
```


Retrieves character formatting previously saved on the stack.

 **Examples:** 

Shows how to use a document builder's formatting stack.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set up font formatting, then write the text that goes before the hyperlink.
 builder.getFont().setName("Arial");
 builder.getFont().setSize(24.0);
 builder.write("To visit Google, hold Ctrl and click ");

 // Preserve our current formatting configuration on the stack.
 builder.pushFont();

 // Alter the builder's current formatting by applying a new style.
 builder.getFont().setStyleIdentifier(StyleIdentifier.HYPERLINK);
 builder.insertHyperlink("here", "http://www.google.com", false);

 Assert.assertEquals(Color.BLUE.getRGB(), builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.SINGLE, builder.getFont().getUnderline());

 // Restore the font formatting that we saved earlier and remove the element from the stack.
 builder.popFont();

 Assert.assertEquals(0, builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.NONE, builder.getFont().getUnderline());

 builder.write(". We hope you enjoyed the example.");

 doc.save(getArtifactsDir() + "DocumentBuilder.PushPopFont.docx");
 
```

### pushFont() {#pushFont}
```
public void pushFont()
```


Saves current character formatting onto the stack.

 **Examples:** 

Shows how to use a document builder's formatting stack.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set up font formatting, then write the text that goes before the hyperlink.
 builder.getFont().setName("Arial");
 builder.getFont().setSize(24.0);
 builder.write("To visit Google, hold Ctrl and click ");

 // Preserve our current formatting configuration on the stack.
 builder.pushFont();

 // Alter the builder's current formatting by applying a new style.
 builder.getFont().setStyleIdentifier(StyleIdentifier.HYPERLINK);
 builder.insertHyperlink("here", "http://www.google.com", false);

 Assert.assertEquals(Color.BLUE.getRGB(), builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.SINGLE, builder.getFont().getUnderline());

 // Restore the font formatting that we saved earlier and remove the element from the stack.
 builder.popFont();

 Assert.assertEquals(0, builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.NONE, builder.getFont().getUnderline());

 builder.write(". We hope you enjoyed the example.");

 doc.save(getArtifactsDir() + "DocumentBuilder.PushPopFont.docx");
 
```

### removeParaAttr(int key) {#removeParaAttr-int}
```
public void removeParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### resetToDefaultAttrs() {#resetToDefaultAttrs}
```
public void resetToDefaultAttrs()
```




### setBold(boolean value) {#setBold-boolean}
```
public void setBold(boolean value)
```


True if the font is formatted as bold.

 **Examples:** 

Shows how to fill MERGEFIELDs with data with a document builder instead of a mail merge.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
 // and then fill them manually.
 builder.insertField(" MERGEFIELD Chairman ");
 builder.insertField(" MERGEFIELD ChiefFinancialOfficer ");
 builder.insertField(" MERGEFIELD ChiefTechnologyOfficer ");

 builder.moveToMergeField("Chairman");
 builder.setBold(true);
 builder.writeln("John Doe");

 builder.moveToMergeField("ChiefFinancialOfficer");
 builder.setItalic(true);
 builder.writeln("Jane Doe");

 builder.moveToMergeField("ChiefTechnologyOfficer");
 builder.setItalic(true);
 builder.writeln("John Bloggs");

 doc.save(getArtifactsDir() + "DocumentBuilder.FillMergeFields.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setCellAttr(int key, Object value) {#setCellAttr-int-java.lang.Object}
```
public void setCellAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setDocument(Document value) {#setDocument-com.aspose.words.Document}
```
public void setDocument(Document value)
```


Sets the [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) object that this object is attached to.

 **Examples:** 

Shows how to apply and revert page setup settings to sections in a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [Document](../../com.aspose.words/document/) | The [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) object that this object is attached to. |

### setItalic(boolean value) {#setItalic-boolean}
```
public void setItalic(boolean value)
```


True if the font is formatted as italic.

 **Examples:** 

Shows how to fill MERGEFIELDs with data with a document builder instead of a mail merge.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
 // and then fill them manually.
 builder.insertField(" MERGEFIELD Chairman ");
 builder.insertField(" MERGEFIELD ChiefFinancialOfficer ");
 builder.insertField(" MERGEFIELD ChiefTechnologyOfficer ");

 builder.moveToMergeField("Chairman");
 builder.setBold(true);
 builder.writeln("John Doe");

 builder.moveToMergeField("ChiefFinancialOfficer");
 builder.setItalic(true);
 builder.writeln("Jane Doe");

 builder.moveToMergeField("ChiefTechnologyOfficer");
 builder.setItalic(true);
 builder.writeln("John Bloggs");

 doc.save(getArtifactsDir() + "DocumentBuilder.FillMergeFields.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object}
```
public void setParaAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setRowAttr(int key, Object value) {#setRowAttr-int-java.lang.Object}
```
public void setRowAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setRunAttr(int fontAttr, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int fontAttr, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |
| value | java.lang.Object |  |

### setUnderline(int value) {#setUnderline-int}
```
public void setUnderline(int value)
```


Gets/sets underline type for the current font.

 **Examples:** 

Shows how to format text inserted by a document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.setUnderline(Underline.DASH);
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setSize(32.0);

 // The builder applies formatting to its current paragraph and any new text added by it afterward.
 builder.writeln("Large, blue, and underlined text.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertUnderline.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [Underline](../../com.aspose.words/underline/) constants. |

### startBookmark(String bookmarkName) {#startBookmark-java.lang.String}
```
public BookmarkStart startBookmark(String bookmarkName)
```


Marks the current position in the document as a bookmark start.

 **Remarks:** 

Bookmarks in a document can overlap and span any range. To create a valid bookmark you need to call both [startBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#startBookmark-java.lang.String) and [endBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#endBookmark-java.lang.String) with the same  bookmarkName  parameter.

Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.

 **Examples:** 

Shows how create a bookmark.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A valid bookmark needs to have document body text enclosed by
 // BookmarkStart and BookmarkEnd nodes created with a matching bookmark name.
 builder.startBookmark("MyBookmark");
 builder.writeln("Hello world!");
 builder.endBookmark("MyBookmark");

 Assert.assertEquals(1, doc.getRange().getBookmarks().getCount());
 Assert.assertEquals("MyBookmark", doc.getRange().getBookmarks().get(0).getName());
 Assert.assertEquals("Hello world!", doc.getRange().getBookmarks().get(0).getText().trim());
 
```

Shows how to insert a hyperlink which references a local bookmark.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startBookmark("Bookmark1");
 builder.write("Bookmarked text. ");
 builder.endBookmark("Bookmark1");
 builder.writeln("Text outside of the bookmark.");

 // Insert a HYPERLINK field that links to the bookmark. We can pass field switches
 // to the "InsertHyperlink" method as part of the argument containing the referenced bookmark's name.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 builder.insertHyperlink("Link to Bookmark1", "Bookmark1\" \\o \"Hyperlink Tip", true);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | Name of the bookmark. |

**Returns:**
[BookmarkStart](../../com.aspose.words/bookmarkstart/) - The bookmark start node that was just created.
### startColumnBookmark(String bookmarkName) {#startColumnBookmark-java.lang.String}
```
public BookmarkStart startColumnBookmark(String bookmarkName)
```


Marks the current position in the document as a column bookmark start. The position must be in a table cell.

 **Remarks:** 

A column bookmark covers one or more columns in a range of rows. To create a valid bookmark you need to call both [startColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#startColumnBookmark-java.lang.String) and [endColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#endColumnBookmark-java.lang.String) with the same  bookmarkName  parameter.

Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.

The actual position of the inserted [BookmarkStart](../../com.aspose.words/bookmarkstart/) node may differ from the current document builder position.

 **Examples:** 

Shows how to create a column bookmark.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 builder.insertCell();
 // Cells 1,2,4,5 will be bookmarked.
 builder.startColumnBookmark("MyBookmark_1");
 // Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.
 builder.startColumnBookmark("MyBookmark_1");
 builder.startColumnBookmark("BadStartBookmark");
 builder.write("Cell 1");

 builder.insertCell();
 builder.write("Cell 2");

 builder.insertCell();
 builder.write("Cell 3");

 builder.endRow();

 builder.insertCell();
 builder.write("Cell 4");

 builder.insertCell();
 builder.write("Cell 5");
 builder.endColumnBookmark("MyBookmark_1");
 builder.endColumnBookmark("MyBookmark_1");

 builder.insertCell();
 builder.write("Cell 6");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "Bookmarks.CreateColumnBookmark.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | Name of the bookmark. |

**Returns:**
[BookmarkStart](../../com.aspose.words/bookmarkstart/) - The bookmark start node that was just created.
### startEditableRange() {#startEditableRange}
```
public EditableRangeStart startEditableRange()
```


Marks the current position in the document as an editable range start.

 **Remarks:** 

Editable range in a document can overlap and span any range. To create a valid editable range you need to call both [startEditableRange()](../../com.aspose.words/documentbuilder/\#startEditableRange) and [endEditableRange()](../../com.aspose.words/documentbuilder/\#endEditableRange) or [endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder/\#endEditableRange-com.aspose.words.EditableRangeStart) methods.

Badly formed editable range will be ignored when the document is saved.

 **Examples:** 

Shows how to create nested editable ranges.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "MyPassword");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! Since we have set the document's protection level to read-only, " +
         "we cannot edit this paragraph without the password.");

 // Create two nested editable ranges.
 EditableRangeStart outerEditableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph inside the outer editable range and can be edited.");

 EditableRangeStart innerEditableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

 // Currently, the document builder's node insertion cursor is in more than one ongoing editable range.
 // When we want to end an editable range in this situation,
 // we need to specify which of the ranges we wish to end by passing its EditableRangeStart node.
 builder.endEditableRange(innerEditableRangeStart);

 builder.writeln("This paragraph inside the outer editable range and can be edited.");

 builder.endEditableRange(outerEditableRangeStart);

 builder.writeln("This paragraph is outside any editable ranges, and cannot be edited.");

 // If a region of text has two overlapping editable ranges with specified groups,
 // the combined group of users excluded by both groups are prevented from editing it.
 outerEditableRangeStart.getEditableRange().setEditorGroup(EditorType.EVERYONE);
 innerEditableRangeStart.getEditableRange().setEditorGroup(EditorType.CONTRIBUTORS);

 doc.save(getArtifactsDir() + "EditableRange.Nested.docx");
 
```

Shows how to work with an editable range.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "MyPassword");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! Since we have set the document's protection level to read-only," +
         " we cannot edit this paragraph without the password.");

 // Editable ranges allow us to leave parts of protected documents open for editing.
 EditableRangeStart editableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph is inside an editable range, and can be edited.");
 EditableRangeEnd editableRangeEnd = builder.endEditableRange();

 // A well-formed editable range has a start node, and end node.
 // These nodes have matching IDs and encompass editable nodes.
 EditableRange editableRange = editableRangeStart.getEditableRange();

 Assert.assertEquals(editableRangeStart.getId(), editableRange.getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getId());

 // Different parts of the editable range link to each other.
 Assert.assertEquals(editableRangeStart.getId(), editableRange.getEditableRangeStart().getId());
 Assert.assertEquals(editableRangeStart.getId(), editableRangeEnd.getEditableRangeStart().getId());
 Assert.assertEquals(editableRange.getId(), editableRangeStart.getEditableRange().getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getEditableRangeEnd().getId());

 // We can access the node types of each part like this. The editable range itself is not a node,
 // but an entity which consists of a start, an end, and their enclosed contents.
 Assert.assertEquals(NodeType.EDITABLE_RANGE_START, editableRangeStart.getNodeType());
 Assert.assertEquals(NodeType.EDITABLE_RANGE_END, editableRangeEnd.getNodeType());

 builder.writeln("This paragraph is outside the editable range, and cannot be edited.");

 doc.save(getArtifactsDir() + "EditableRange.CreateAndRemove.docx");

 // Remove an editable range. All the nodes that were inside the range will remain intact.
 editableRange.remove();
 
```

**Returns:**
[EditableRangeStart](../../com.aspose.words/editablerangestart/) - The editable range start node that was just created.
### startTable() {#startTable}
```
public Table startTable()
```


Starts a table in the document.

 **Remarks:** 

The next method to call is [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell).

This method starts a nested table when called inside a cell.

 **Examples:** 

Shows how to build a table with custom borders.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Shows how to format cells with a document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

Shows how to build a formatted 2x2 table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

**Returns:**
[Table](../../com.aspose.words/table/) - The table node that was just created.
### write(String text) {#write-java.lang.String}
```
public void write(String text)
```


Inserts a string into the document at the current insert position.

 **Remarks:** 

Current font formatting specified by the [getFont()](../../com.aspose.words/documentbuilder/\#getFont) property is used.

 **Examples:** 

Shows how to insert a string surrounded by a border into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

Shows how to use a document builder to create a table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Start the table, then populate the first row with two cells.
 builder.startTable();
 builder.insertCell();
 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");

 // Call the builder's "EndRow" method to start a new row.
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateTable.docx");
 
```

Shows how to build a table with custom borders.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Shows how to build a formatted 2x2 table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| text | java.lang.String | The string to insert into the document. |

### writeln() {#writeln}
```
public void writeln()
```


Inserts a paragraph break into the document.

 **Remarks:** 

Calls [insertParagraph()](../../com.aspose.words/documentbuilder/\#insertParagraph).

 **Examples:** 

Shows how to create headers and footers in a document using DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

### writeln(String text) {#writeln-java.lang.String}
```
public void writeln(String text)
```


Inserts a string and a paragraph break into the document.

 **Remarks:** 

Current font and paragraph formatting specified by the [getFont()](../../com.aspose.words/documentbuilder/\#getFont) and [getParagraphFormat()](../../com.aspose.words/documentbuilder/\#getParagraphFormat) properties are used.

 **Examples:** 

Shows how to build a formatted 2x2 table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| text | java.lang.String | The string to insert into the document. |

