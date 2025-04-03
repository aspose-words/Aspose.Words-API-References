---
title: DocumentBuilder class
linktitle: DocumentBuilder class
articleTitle: DocumentBuilder class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.DocumentBuilder class. Provides methods to insert text, images and other content, specify font, paragraph and section formatting"
type: docs
weight: 330
url: /nodejs-net/Aspose.Words/documentbuilder/
---

## DocumentBuilder class

Provides methods to insert text, images and other content, specify font, paragraph and section formatting.
To learn more, visit the [Document Builder Overview](https://docs.aspose.com/words/nodejs-net/document-builder-overview/) documentation article.




### Remarks

[DocumentBuilder](./) makes the process of building a [Document](../document/) easier.
[Document](../document/) is a composite object consisting of a tree of nodes and while inserting content
nodes directly into the tree is possible, it requires good understanding of the tree structure.
[DocumentBuilder](./) is a "facade" for the complex structure of [Document](../document/) and allows
to insert content and formatting quickly and easily.

Create a [DocumentBuilder](./) and associate it with a [Document](../document/).

The [DocumentBuilder](./) has an internal cursor where the text will be inserted
when you call [DocumentBuilder.write()](./write/#string), [DocumentBuilder.writeln()](./writeln/#string), [DocumentBuilder.insertBreak()](./insertBreak/#breaktype)
and other methods. You can navigate the [DocumentBuilder](./) cursor to a different location
in a document using various MoveToXXX methods.

Use the [DocumentBuilder.font](./font/) property to specify character formatting that will apply to
all text inserted from the current position in the document onwards.

Use the [DocumentBuilder.paragraphFormat](./paragraphFormat/) property to specify paragraph formatting for the current
and all paragraphs that will be inserted.

Use the [DocumentBuilder.pageSetup](./pageSetup/) property to specify page and section properties for the current
section and all section that will be inserted.

Use the [DocumentBuilder.cellFormat](./cellFormat/) and [DocumentBuilder.rowFormat](./rowFormat/) properties to specify
formatting properties for table cells and rows. User the [DocumentBuilder.insertCell()](./insertCell/#default) and
[DocumentBuilder.endRow()](./endRow/#default) methods to build a table.

Note that [DocumentBuilder.font](./font/), [DocumentBuilder.paragraphFormat](./paragraphFormat/) and [DocumentBuilder.pageSetup](./pageSetup/) properties are updated whenever
you navigate to a different place in the document to reflect formatting properties available at the new location.




### Constructors
| Name | Description |
| --- | --- |
| [DocumentBuilder()](./constructor/#default) | Initializes a new instance of this class. |
| [DocumentBuilder(options)](./constructor/#documentbuilderoptions) | Initializes a new instance of this class. |
| [DocumentBuilder(doc)](./constructor/#document) | Initializes a new instance of this class. |
| [DocumentBuilder(doc, options)](./constructor/#document_documentbuilderoptions) | Initializes a new instance of this class. |

### Properties

| Name | Description |
| --- | --- |
| [bold](./bold/) | True if the font is formatted as bold. |
| [cellFormat](./cellFormat/) | Returns an object that represents current table cell formatting properties. |
| [currentNode](./currentNode/) | Gets the node that is currently selected in this DocumentBuilder. |
| [currentParagraph](./currentParagraph/) | Gets the paragraph that is currently selected in this [DocumentBuilder](./). |
| [currentSection](./currentSection/) | Gets the section that is currently selected in this [DocumentBuilder](./). |
| [currentStory](./currentStory/) | Gets the story that is currently selected in this [DocumentBuilder](./). |
| [currentStructuredDocumentTag](./currentStructuredDocumentTag/) | Gets the structured document tag that is currently selected in this [DocumentBuilder](./). |
| [document](./document/) | Gets or sets the [DocumentBuilder.document](./document/) object that this object is attached to. |
| [font](./font/) | Returns an object that represents current font formatting properties. |
| [isAtEndOfParagraph](./isAtEndOfParagraph/) | Returns ``true`` if the cursor is at the end of the current paragraph. |
| [isAtEndOfStructuredDocumentTag](./isAtEndOfStructuredDocumentTag/) | Returns **true** if the cursor is at the end of a structured document tag. |
| [isAtStartOfParagraph](./isAtStartOfParagraph/) | Returns ``true`` if the cursor is at the beginning of the current paragraph (no text before the cursor). |
| [italic](./italic/) | True if the font is formatted as italic. |
| [listFormat](./listFormat/) | Returns an object that represents current list formatting properties. |
| [pageSetup](./pageSetup/) | Returns an object that represents current page setup and section properties. |
| [paragraphFormat](./paragraphFormat/) | Returns an object that represents current paragraph formatting properties. |
| [rowFormat](./rowFormat/) | Returns an object that represents current table row formatting properties. |
| [underline](./underline/) | Gets/sets underline type for the current font. |

### Methods

| Name | Description |
| --- | --- |
|[ deleteRow(tableIndex, rowIndex)](./deleteRow/#number_number) | Deletes a row from a table. |
|[ endBookmark(bookmarkName)](./endBookmark/#string) | Marks the current position in the document as a bookmark end. |
|[ endColumnBookmark(bookmarkName)](./endColumnBookmark/#string) | Marks the current position in the document as a column bookmark end. The position must be in a table cell. |
|[ endEditableRange()](./endEditableRange/#default) | Marks the current position in the document as an editable range end. |
|[ endEditableRange(start)](./endEditableRange/#editablerangestart) | Marks the current position in the document as an editable range end. |
|[ endRow()](./endRow/#default) | Ends a table row in the document. |
|[ endTable()](./endTable/#default) | Ends a table in the document. |
|[ insertBreak(breakType)](./insertBreak/#breaktype) | Inserts a break of the specified type into the document. |
|[ insertCell()](./insertCell/#default) | Inserts a table cell into the document. |
|[ insertChart(chartType, width, height)](./insertChart/#charttype_number_number) | Inserts an chart object into the document and scales it to the specified size. |
|[ insertChart(chartType, horzPos, left, vertPos, top, width, height, wrapType)](./insertChart/#charttype_relativehorizontalposition_number_relativeverticalposition_number_number_number_wraptype) | Inserts an chart object into the document and scales it to the specified size. |
|[ insertCheckBox(name, checkedValue, size)](./insertCheckBox/#string_boolean_number) | Inserts a checkbox form field at the current position. |
|[ insertCheckBox(name, defaultValue, checkedValue, size)](./insertCheckBox/#string_boolean_boolean_number) | Inserts a checkbox form field at the current position. |
|[ insertComboBox(name, items, selectedIndex)](./insertComboBox/#string_string[]_number) | Inserts a combobox form field at the current position. |
|[ insertDocument(srcDoc, importFormatMode)](./insertDocument/#document_importformatmode) | Inserts a document at the cursor position. |
|[ insertDocument(srcDoc, importFormatMode, importFormatOptions)](./insertDocument/#document_importformatmode_importformatoptions) | Inserts a document at the cursor position. |
|[ insertDocumentInline(srcDoc, importFormatMode, importFormatOptions)](./insertDocumentInline/#document_importformatmode_importformatoptions) | Inserts a document inline at the cursor position. |
|[ insertField(fieldType, updateField)](./insertField/#fieldtype_boolean) | Inserts a Word field into a document and optionally updates the field result. |
|[ insertField(fieldCode)](./insertField/#string) | Inserts a Word field into a document and updates the field result. |
|[ insertField(fieldCode, fieldValue)](./insertField/#string_string) | Inserts a Word field into a document without updating the field result. |
|[ insertFootnote(footnoteType, footnoteText)](./insertFootnote/#footnotetype_string) | Inserts a footnote or endnote into the document. |
|[ insertFootnote(footnoteType, footnoteText, referenceMark)](./insertFootnote/#footnotetype_string_string) | Inserts a footnote or endnote into the document. |
|[ insertForms2OleControl(forms2OleControl)](./insertForms2OleControl/#forms2olecontrol) | Inserts [Forms2OleControl](../../aspose.words.drawing.ole/forms2olecontrol/) object into current position. |
|[ insertGroupShape(shapes)](./insertGroupShape/#shapebase[]) | Groups the shapes passed as a parameter into a new GroupShape node which is inserted into the current position. |
|[ insertGroupShape(left, top, width, height, shapes)](./insertGroupShape/#number_number_number_number_shapebase[]) | Groups the shapes passed as a parameter into a new GroupShape node of the specified size which is inserted into the specified position. |
|[ insertHorizontalRule()](./insertHorizontalRule/#default) | Inserts a horizontal rule shape into the document. |
|[ insertHtml(html)](./insertHtml/#string) | Inserts an HTML string into the document. |
|[ insertHtml(html, useBuilderFormatting)](./insertHtml/#string_boolean) | Inserts an HTML string into the document. |
|[ insertHtml(html, options)](./insertHtml/#string_htmlinsertoptions) | Inserts an HTML string into the document. Allows to specify additional options. |
|[ insertHyperlink(displayText, urlOrBookmark, isBookmark)](./insertHyperlink/#string_string_boolean) | Inserts a hyperlink into the document. |
|[ insertImage(image)](./insertImage/#jsimage) |  |
|[ insertImage(image, width, height)](./insertImage/#jsimage_number_number) |  |
|[ insertImage(image, horzPos, left, vertPos, top, width, height, wrapType)](./insertImage/#jsimage_relativehorizontalposition_number_relativeverticalposition_number_number_number_wraptype) |  |
|[ insertImage(fileName)](./insertImage/#string) | Inserts an image from a file or URL into the document. The image is inserted inline and at 100% scale. |
|[ insertImage(stream)](./insertImage/#buffer) | Inserts an image from a stream into the document. The image is inserted inline and at 100% scale. |
|[ insertImage(imageBytes)](./insertImage/#number[]) | Inserts an image from a byte array into the document. The image is inserted inline and at 100% scale. |
|[ insertImage(fileName, width, height)](./insertImage/#string_number_number) | Inserts an inline image from a file or URL into the document and scales it to the specified size. |
|[ insertImage(stream, width, height)](./insertImage/#buffer_number_number) | Inserts an inline image from a stream into the document and scales it to the specified size. |
|[ insertImage(imageBytes, width, height)](./insertImage/#number[]_number_number) | Inserts an inline image from a byte array into the document and scales it to the specified size. |
|[ insertImage(fileName, horzPos, left, vertPos, top, width, height, wrapType)](./insertImage/#string_relativehorizontalposition_number_relativeverticalposition_number_number_number_wraptype) | Inserts an image from a file or URL at the specified position and size. |
|[ insertImage(stream, horzPos, left, vertPos, top, width, height, wrapType)](./insertImage/#buffer_relativehorizontalposition_number_relativeverticalposition_number_number_number_wraptype) | Inserts an image from a stream at the specified position and size. |
|[ insertImage(imageBytes, horzPos, left, vertPos, top, width, height, wrapType)](./insertImage/#number[]_relativehorizontalposition_number_relativeverticalposition_number_number_number_wraptype) | Inserts an image from a byte array at the specified position and size. |
|[ insertNode(node)](./insertNode/#node) | Inserts a node before the cursor. |
|[ insertOleObject(stream, progId, asIcon, presentation)](./insertOleObject/#buffer_string_boolean_buffer) | Inserts an embedded OLE object from a stream into the document. |
|[ insertOleObject(fileName, isLinked, asIcon, presentation)](./insertOleObject/#string_boolean_boolean_buffer) | Inserts an embedded or linked OLE object from a file into the document. Detects OLE object type using file extension. |
|[ insertOleObject(fileName, progId, isLinked, asIcon, presentation)](./insertOleObject/#string_string_boolean_boolean_buffer) | Inserts an embedded or linked OLE object from a file into the document. Detects OLE object type using given progID parameter. |
|[ insertOleObjectAsIcon(fileName, isLinked, iconFile, iconCaption)](./insertOleObjectAsIcon/#string_boolean_string_string) | Inserts an embedded or linked OLE object as icon into the document. Allows to specify icon file and caption. Detects OLE object type using file extension. |
|[ insertOleObjectAsIcon(fileName, progId, isLinked, iconFile, iconCaption)](./insertOleObjectAsIcon/#string_string_boolean_string_string) | Inserts an embedded or linked OLE object as icon into the document. Allows to specify icon file and caption. Detects OLE object type using given progID parameter. |
|[ insertOleObjectAsIcon(stream, progId, iconFile, iconCaption)](./insertOleObjectAsIcon/#buffer_string_string_string) | Inserts an embedded OLE object as icon from a stream into the document. Allows to specify icon file and caption. Detects OLE object type using given progID parameter. |
|[ insertOnlineVideo(videoUrl, width, height)](./insertOnlineVideo/#string_number_number) | Inserts an online video object into the document and scales it to the specified size. |
|[ insertOnlineVideo(videoUrl, horzPos, left, vertPos, top, width, height, wrapType)](./insertOnlineVideo/#string_relativehorizontalposition_number_relativeverticalposition_number_number_number_wraptype) | Inserts an online video object into the document and scales it to the specified size. |
|[ insertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, width, height)](./insertOnlineVideo/#string_string_number[]_number_number) | Inserts an online video object into the document and scales it to the specified size. |
|[ insertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, horzPos, left, vertPos, top, width, height, wrapType)](./insertOnlineVideo/#string_string_number[]_relativehorizontalposition_number_relativeverticalposition_number_number_number_wraptype) | Inserts an online video object into the document and scales it to the specified size. |
|[ insertParagraph()](./insertParagraph/#default) | Inserts a paragraph break into the document. |
|[ insertShape(shapeType, width, height)](./insertShape/#shapetype_number_number) | Inserts inline shape with specified type and size. |
|[ insertShape(shapeType, horzPos, left, vertPos, top, width, height, wrapType)](./insertShape/#shapetype_relativehorizontalposition_number_relativeverticalposition_number_number_number_wraptype) | Inserts free-floating shape with specified position, size and text wrap type. |
|[ insertSignatureLine(signatureLineOptions)](./insertSignatureLine/#signaturelineoptions) | Inserts a signature line at the current position. |
|[ insertSignatureLine(signatureLineOptions, horzPos, left, vertPos, top, wrapType)](./insertSignatureLine/#signaturelineoptions_relativehorizontalposition_number_relativeverticalposition_number_wraptype) | Inserts a signature line at the specified position. |
|[ insertStructuredDocumentTag(type)](./insertStructuredDocumentTag/#sdttype) | Inserts a [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/) into the document. |
|[ insertStyleSeparator()](./insertStyleSeparator/#default) | Inserts style separator into the document. |
|[ insertTableOfContents(switches)](./insertTableOfContents/#string) | Inserts a TOC (table of contents) field into the document. |
|[ insertTextInput(name, type, format, fieldValue, maxLength)](./insertTextInput/#string_textformfieldtype_string_string_number) | Inserts a text form field at the current position. |
|[ moveTo(node)](./moveTo/#node) | Moves the cursor to an inline node or to the end of a paragraph. |
|[ moveToBookmark(bookmarkName)](./moveToBookmark/#string) | Moves the cursor to a bookmark. |
|[ moveToBookmark(bookmarkName, isStart, isAfter)](./moveToBookmark/#string_boolean_boolean) | Moves the cursor to a bookmark with greater precision. |
|[ moveToCell(tableIndex, rowIndex, columnIndex, characterIndex)](./moveToCell/#number_number_number_number) | Moves the cursor to a table cell in the current section. |
|[ moveToDocumentEnd()](./moveToDocumentEnd/#default) | Moves the cursor to the end of the document. |
|[ moveToDocumentStart()](./moveToDocumentStart/#default) | Moves the cursor to the beginning of the document. |
|[ moveToField(field, isAfter)](./moveToField/#field_boolean) | Moves the cursor to a field in the document. |
|[ moveToHeaderFooter(headerFooterType)](./moveToHeaderFooter/#headerfootertype) | Moves the cursor to the beginning of a header or footer in the current section. |
|[ moveToMergeField(fieldName)](./moveToMergeField/#string) | Moves the cursor to a position just beyond the specified merge field and removes the merge field. |
|[ moveToMergeField(fieldName, isAfter, isDeleteField)](./moveToMergeField/#string_boolean_boolean) | Moves the merge field to the specified merge field. |
|[ moveToParagraph(paragraphIndex, characterIndex)](./moveToParagraph/#number_number) | Moves the cursor to a paragraph in the current section. |
|[ moveToSection(sectionIndex)](./moveToSection/#number) | Moves the cursor to the beginning of the body in a specified section. |
|[ moveToStructuredDocumentTag(structuredDocumentTagIndex, characterIndex)](./moveToStructuredDocumentTag/#number_number) | Moves the cursor to a structured document tag in the current section. |
|[ moveToStructuredDocumentTag(structuredDocumentTag, characterIndex)](./moveToStructuredDocumentTag/#structureddocumenttag_number) | Moves the cursor to the structured document tag. |
|[ popFont()](./popFont/#default) | Retrieves character formatting previously saved on the stack. |
|[ pushFont()](./pushFont/#default) | Saves current character formatting onto the stack. |
|[ startBookmark(bookmarkName)](./startBookmark/#string) | Marks the current position in the document as a bookmark start. |
|[ startColumnBookmark(bookmarkName)](./startColumnBookmark/#string) | Marks the current position in the document as a column bookmark start. The position must be in a table cell. |
|[ startEditableRange()](./startEditableRange/#default) | Marks the current position in the document as an editable range start. |
|[ startTable()](./startTable/#default) | Starts a table in the document. |
|[ write(text)](./write/#string) | Inserts a string into the document at the current insert position. |
|[ writeln(text)](./writeln/#string) | Inserts a string and a paragraph break into the document. |
|[ writeln()](./writeln/#default) | Inserts a paragraph break into the document. |

### Examples

Shows how to create headers and footers in a document using DocumentBuilder.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Specify that we want different headers and footers for first, even and odd pages.
builder.pageSetup.differentFirstPageHeaderFooter = true;
builder.pageSetup.oddAndEvenPagesHeaderFooter = true;

// Create the headers, then add three pages to the document to display each header type.
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderFirst);
builder.write("Header for the first page");
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderEven);
builder.write("Header for even pages");
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderPrimary);
builder.write("Header for all other pages");

builder.moveToSection(0);
builder.writeln("Page1");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page2");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page3");

doc.save(base.artifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

Shows how to build a table with custom borders.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.startTable();

// Setting table formatting options for a document builder
// will apply them to every row and cell that we add with it.
builder.paragraphFormat.alignment = aw.ParagraphAlignment.Center;

builder.cellFormat.clearFormatting();
builder.cellFormat.width = 150;
builder.cellFormat.verticalAlignment = aw.Tables.CellVerticalAlignment.Center;
builder.cellFormat.shading.backgroundPatternColor = "#ADFF2F";
builder.cellFormat.wrapText = false;
builder.cellFormat.fitText = true;

builder.rowFormat.clearFormatting();
builder.rowFormat.heightRule = aw.HeightRule.Exactly;
builder.rowFormat.height = 50;
builder.rowFormat.borders.lineStyle = aw.LineStyle.Engrave3D;
builder.rowFormat.borders.color = "#FFA500";

builder.insertCell();
builder.write("Row 1, Col 1");

builder.insertCell();
builder.write("Row 1, Col 2");
builder.endRow();

// Changing the formatting will apply it to the current cell,
// and any new cells that we create with the builder afterward.
// This will not affect the cells that we have added previously.
builder.cellFormat.shading.clearFormatting();

builder.insertCell();
builder.write("Row 2, Col 1");

builder.insertCell();
builder.write("Row 2, Col 2");

builder.endRow();

// Increase row height to fit the vertical text.
builder.insertCell();
builder.rowFormat.height = 150;
builder.cellFormat.orientation = aw.TextOrientation.Upward;
builder.write("Row 3, Col 1");

builder.insertCell();
builder.cellFormat.orientation = aw.TextOrientation.Downward;
builder.write("Row 3, Col 2");

builder.endRow();
builder.endTable();

doc.save(base.artifactsDir + "DocumentBuilder.InsertTable.docx");
```

Shows how to use a document builder to create a table.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

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

doc.save(base.artifactsDir + "DocumentBuilder.CreateTable.docx");
```

### See Also

* module [Aspose.Words](../)

