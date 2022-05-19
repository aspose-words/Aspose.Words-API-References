---
title: DocumentBuilder
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 440
url: /net/aspose.words/documentbuilder/
---
## DocumentBuilder class

Provides methods to insert text, images and other content, specify font, paragraph and section formatting.

```csharp
public class DocumentBuilder
```

## Constructors

| Name | Description |
| --- | --- |
| [DocumentBuilder](documentbuilder)() | Initializes a new instance of this class. |
| [DocumentBuilder](documentbuilder)(Document) | Initializes a new instance of this class. |

## Properties

| Name | Description |
| --- | --- |
| [Bold](../../aspose.words/documentbuilder/bold) { get; set; } | True if the font is formatted as bold. |
| [CellFormat](../../aspose.words/documentbuilder/cellformat) { get; } | Returns an object that represents current table cell formatting properties. |
| [CurrentNode](../../aspose.words/documentbuilder/currentnode) { get; } | Gets the node that is currently selected in this DocumentBuilder. |
| [CurrentParagraph](../../aspose.words/documentbuilder/currentparagraph) { get; } | Gets the paragraph that is currently selected in this DocumentBuilder. |
| [CurrentSection](../../aspose.words/documentbuilder/currentsection) { get; } | Gets the section that is currently selected in this DocumentBuilder. |
| [CurrentStory](../../aspose.words/documentbuilder/currentstory) { get; } | Gets the story that is currently selected in this DocumentBuilder. |
| [Document](../../aspose.words/documentbuilder/document) { get; set; } | Gets or sets the [`Document`](./document) object that this object is attached to. |
| [Font](../../aspose.words/documentbuilder/font) { get; } | Returns an object that represents current font formatting properties. |
| [IsAtEndOfParagraph](../../aspose.words/documentbuilder/isatendofparagraph) { get; } | Returns true if the cursor is at the end of the current paragraph. |
| [IsAtStartOfParagraph](../../aspose.words/documentbuilder/isatstartofparagraph) { get; } | Returns true if the cursor is at the beginning of the current paragraph (no text before the cursor). |
| [Italic](../../aspose.words/documentbuilder/italic) { get; set; } | True if the font is formatted as italic. |
| [ListFormat](../../aspose.words/documentbuilder/listformat) { get; } | Returns an object that represents current list formatting properties. |
| [PageSetup](../../aspose.words/documentbuilder/pagesetup) { get; } | Returns an object that represents current page setup and section properties. |
| [ParagraphFormat](../../aspose.words/documentbuilder/paragraphformat) { get; } | Returns an object that represents current paragraph formatting properties. |
| [RowFormat](../../aspose.words/documentbuilder/rowformat) { get; } | Returns an object that represents current table row formatting properties. |
| [Underline](../../aspose.words/documentbuilder/underline) { get; set; } | Gets/sets underline type for the current font. |

## Methods

| Name | Description |
| --- | --- |
| [DeleteRow](../../aspose.words/documentbuilder/deleterow)(int, int) | Deletes a row from a table. |
| [EndBookmark](../../aspose.words/documentbuilder/endbookmark)(string) | Marks the current position in the document as a bookmark end. |
| [EndColumnBookmark](../../aspose.words/documentbuilder/endcolumnbookmark)(string) | Marks the current position in the document as a column bookmark end. The position must be in a table cell. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange)() | Marks the current position in the document as an editable range end. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange)(EditableRangeStart) | Marks the current position in the document as an editable range end. |
| [EndRow](../../aspose.words/documentbuilder/endrow)() | Ends a table row in the document. |
| [EndTable](../../aspose.words/documentbuilder/endtable)() | Ends a table in the document. |
| [InsertBreak](../../aspose.words/documentbuilder/insertbreak)(BreakType) | Inserts a break of the specified type into the document. |
| [InsertCell](../../aspose.words/documentbuilder/insertcell)() | Inserts a table cell into the document. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart)(ChartType, double, double) | Inserts an chart object into the document and scales it to the specified size. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart)(ChartType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserts an chart object into the document and scales it to the specified size. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox)(string, bool, int) | Inserts a checkbox form field at the current position. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox)(string, bool, bool, int) | Inserts a checkbox form field at the current position. |
| [InsertComboBox](../../aspose.words/documentbuilder/insertcombobox)(string, string[], int) | Inserts a combobox form field at the current position. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument)(Document, ImportFormatMode) | Inserts a document at the cursor position. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument)(Document, ImportFormatMode, ImportFormatOptions) | Inserts a document at the cursor position. |
| [InsertField](../../aspose.words/documentbuilder/insertfield)(string) | Inserts a Word field into a document and updates the field result. |
| [InsertField](../../aspose.words/documentbuilder/insertfield)(FieldType, bool) | Inserts a Word field into a document and optionally updates the field result. |
| [InsertField](../../aspose.words/documentbuilder/insertfield)(string, string) | Inserts a Word field into a document without updating the field result. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote)(FootnoteType, string) | Inserts a footnote or endnote into the document. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote)(FootnoteType, string, string) | Inserts a footnote or endnote into the document. |
| [InsertHorizontalRule](../../aspose.words/documentbuilder/inserthorizontalrule)() | Inserts a horizontal rule shape into the document. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml)(string) | Inserts an HTML string into the document. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml)(string, bool) | Inserts an HTML string into the document. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml)(string, HtmlInsertOptions) | Inserts an HTML string into the document. Allows to specify additional options. |
| [InsertHyperlink](../../aspose.words/documentbuilder/inserthyperlink)(string, string, bool) | Inserts a hyperlink into the document. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage)(byte[]) | Inserts an image from a byte array into the document. The image is inserted inline and at 100% scale. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage)(Image) | Inserts an image from a .NET Image object into the document. The image is inserted inline and at 100% scale. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage)(Stream) | Inserts an image from a stream into the document. The image is inserted inline and at 100% scale. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage)(string) | Inserts an image from a file or URL into the document. The image is inserted inline and at 100% scale. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage)(byte[], double, double) | Inserts an inline image from a byte array into the document and scales it to the specified size. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage)(Image, double, double) | Inserts an inline image from a .NET Image object into the document and scales it to the specified size. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage)(Stream, double, double) | Inserts an inline image from a stream into the document and scales it to the specified size. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage)(string, double, double) | Inserts an inline image from a file or URL into the document and scales it to the specified size. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage)(byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserts an image from a byte array at the specified position and size. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage)(Image, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserts an image from a .NET Image object at the specified position and size. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage)(Stream, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserts an image from a stream at the specified position and size. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserts an image from a file or URL at the specified position and size. |
| [InsertNode](../../aspose.words/documentbuilder/insertnode)(Node) | Inserts a text level node inside the current paragraph before the cursor. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject)(Stream, string, bool, Stream) | Inserts an embedded OLE object from a stream into the document. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject)(string, bool, bool, Stream) | Inserts an embedded or linked OLE object from a file into the document. Detects OLE object type using file extension. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject)(string, string, bool, bool, Stream) | Inserts an embedded or linked OLE object from a file into the document. Detects OLE object type using given progID parameter. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon)(Stream, string, string, string) | Inserts an embedded OLE object as icon from a stream into the document. Allows to specify icon file and caption. Detects OLE object type using given progID parameter. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon)(string, bool, string, string) | Inserts an embedded or linked OLE object as icon into the document. Allows to specify icon file and caption. Detects OLE object type using file extension. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon)(string, string, bool, string, string) | Inserts an embedded or linked OLE object as icon into the document. Allows to specify icon file and caption. Detects OLE object type using given progID parameter. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo)(string, double, double) | Inserts an online video object into the document and scales it to the specified size. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo)(string, string, byte[], double, double) | Inserts an online video object into the document and scales it to the specified size. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserts an online video object into the document and scales it to the specified size. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo)(string, string, byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserts an online video object into the document and scales it to the specified size. |
| [InsertParagraph](../../aspose.words/documentbuilder/insertparagraph)() | Inserts a paragraph break into the document. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape)(ShapeType, double, double) | Inserts inline shape with specified type and size. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape)(ShapeType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserts free-floating shape with specified position, size and text wrap type. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline)(SignatureLineOptions) | Inserts a signature line at the current position. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline)(SignatureLineOptions, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, WrapType) | Inserts a signature line at the specified position. |
| [InsertStyleSeparator](../../aspose.words/documentbuilder/insertstyleseparator)() | Inserts style separator into the document. |
| [InsertTableOfContents](../../aspose.words/documentbuilder/inserttableofcontents)(string) | Inserts a TOC (table of contents) field into the document. |
| [InsertTextInput](../../aspose.words/documentbuilder/inserttextinput)(string, TextFormFieldType, string, string, int) | Inserts a text form field at the current position. |
| [MoveTo](../../aspose.words/documentbuilder/moveto)(Node) | Moves the cursor to an inline node or to the end of a paragraph. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark)(string) | Moves the cursor to a bookmark. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark)(string, bool, bool) | Moves the cursor to a bookmark with greater precision. |
| [MoveToCell](../../aspose.words/documentbuilder/movetocell)(int, int, int, int) | Moves the cursor to a table cell in the current section. |
| [MoveToDocumentEnd](../../aspose.words/documentbuilder/movetodocumentend)() | Moves the cursor to the end of the document. |
| [MoveToDocumentStart](../../aspose.words/documentbuilder/movetodocumentstart)() | Moves the cursor to the beginning of the document. |
| [MoveToField](../../aspose.words/documentbuilder/movetofield)(Field, bool) | Moves the cursor to a field in the document. |
| [MoveToHeaderFooter](../../aspose.words/documentbuilder/movetoheaderfooter)(HeaderFooterType) | Moves the cursor to the beginning of a header or footer in the current section. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield)(string) | Moves the cursor to a position just beyond the specified merge field and removes the merge field. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield)(string, bool, bool) | Moves the merge field to the specified merge field. |
| [MoveToParagraph](../../aspose.words/documentbuilder/movetoparagraph)(int, int) | Moves the cursor to a paragraph in the current section. |
| [MoveToSection](../../aspose.words/documentbuilder/movetosection)(int) | Moves the cursor to the beginning of the body in a specified section. |
| [PopFont](../../aspose.words/documentbuilder/popfont)() | Retrieves character formatting previously saved on the stack. |
| [PushFont](../../aspose.words/documentbuilder/pushfont)() | Saves current character formatting onto the stack. |
| [StartBookmark](../../aspose.words/documentbuilder/startbookmark)(string) | Marks the current position in the document as a bookmark start. |
| [StartColumnBookmark](../../aspose.words/documentbuilder/startcolumnbookmark)(string) | Marks the current position in the document as a column bookmark start. The position must be in a table cell. |
| [StartEditableRange](../../aspose.words/documentbuilder/starteditablerange)() | Marks the current position in the document as an editable range start. |
| [StartTable](../../aspose.words/documentbuilder/starttable)() | Starts a table in the document. |
| [Write](../../aspose.words/documentbuilder/write)(string) | Inserts a string into the document at the current insert position. |
| [Writeln](../../aspose.words/documentbuilder/writeln)() | Inserts a paragraph break into the document. |
| [Writeln](../../aspose.words/documentbuilder/writeln)(string) | Inserts a string and a paragraph break into the document. |

### Remarks

**DocumentBuilder** makes the process of building a **Document** easier. **Document** is a composite object consisting of a tree of nodes and while inserting content nodes directly into the tree is possible, it requires good understanding of the tree structure. **DocumentBuilder** is a "facade" for the complex structure of **Document** and allows to insert content and formatting quickly and easily.

Create a **DocumentBuilder** and associate it with a [`Document`](./document).

The **DocumentBuilder** has an internal cursor where the text will be inserted when you call [`Write`](./write), [`Writeln`](./writeln), [`InsertBreak`](./insertbreak) and other methods. You can navigate the **DocumentBuilder** cursor to a different location in a document using various MoveToXXX methods.

Use the [`Font`](./font) property to specify character formatting that will apply to all text inserted from the current position in the document onwards.

Use the [`ParagraphFormat`](./paragraphformat) property to specify paragraph formatting for the current and all paragraphs that will be inserted.

Use the [`PageSetup`](./pagesetup) property to specify page and section properties for the current section and all section that will be inserted.

Use the [`CellFormat`](./cellformat) and [`RowFormat`](./rowformat) properties to specify formatting properties for table cells and rows. User the [`InsertCell`](./insertcell) and [`EndRow`](./endrow) methods to build a table.

Note that **Font**, **ParagraphFormat** and **PageSetup** properties are updated whenever you navigate to a different place in the document to reflect formatting properties available at the new location.

### Examples

Shows how to use a document builder to create a table.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Start the table, then populate the first row with two cells.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

// Call the builder's "EndRow" method to start a new row.
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateTable.docx");
```

Shows how to create headers and footers in a document using DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Specify that we want different headers and footers for first, even and odd pages.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Create the headers, then add three pages to the document to display each header type.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

Shows how to build a table with custom borders.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Setting table formatting options for a document builder
// will apply them to every row and cell that we add with it.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

builder.CellFormat.ClearFormatting();
builder.CellFormat.Width = 150;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.CellFormat.Shading.BackgroundPatternColor = Color.GreenYellow;
builder.CellFormat.WrapText = false;
builder.CellFormat.FitText = true;

builder.RowFormat.ClearFormatting();
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.RowFormat.Height = 50;
builder.RowFormat.Borders.LineStyle = LineStyle.Engrave3D;
builder.RowFormat.Borders.Color = Color.Orange;

builder.InsertCell();
builder.Write("Row 1, Col 1");

builder.InsertCell();
builder.Write("Row 1, Col 2");
builder.EndRow();

// Changing the formatting will apply it to the current cell,
// and any new cells that we create with the builder afterward.
// This will not affect the cells that we have added previously.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Increase row height to fit the vertical text.
builder.InsertCell();
builder.RowFormat.Height = 150;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 3, Col 1");

builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 3, Col 2");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTable.docx");
```

### See Also

* namespace [Aspose.Words](../../aspose.words)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
