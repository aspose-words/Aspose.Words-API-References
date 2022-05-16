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
| [Bold](bold) { get; set; } | True if the font is formatted as bold. |
| [CellFormat](cellformat) { get; } | Returns an object that represents current table cell formatting properties. |
| [CurrentNode](currentnode) { get; } | Gets the node that is currently selected in this DocumentBuilder. |
| [CurrentParagraph](currentparagraph) { get; } | Gets the paragraph that is currently selected in this DocumentBuilder. |
| [CurrentSection](currentsection) { get; } | Gets the section that is currently selected in this DocumentBuilder. |
| [CurrentStory](currentstory) { get; } | Gets the story that is currently selected in this DocumentBuilder. |
| [Document](document) { get; set; } | Gets or sets the [`Document`](./document) object that this object is attached to. |
| [Font](font) { get; } | Returns an object that represents current font formatting properties. |
| [IsAtEndOfParagraph](isatendofparagraph) { get; } | Returns true if the cursor is at the end of the current paragraph. |
| [IsAtStartOfParagraph](isatstartofparagraph) { get; } | Returns true if the cursor is at the beginning of the current paragraph (no text before the cursor). |
| [Italic](italic) { get; set; } | True if the font is formatted as italic. |
| [ListFormat](listformat) { get; } | Returns an object that represents current list formatting properties. |
| [PageSetup](pagesetup) { get; } | Returns an object that represents current page setup and section properties. |
| [ParagraphFormat](paragraphformat) { get; } | Returns an object that represents current paragraph formatting properties. |
| [RowFormat](rowformat) { get; } | Returns an object that represents current table row formatting properties. |
| [Underline](underline) { get; set; } | Gets/sets underline type for the current font. |

## Methods

| Name | Description |
| --- | --- |
| [DeleteRow](deleterow)(int, int) | Deletes a row from a table. |
| [EndBookmark](endbookmark)(string) | Marks the current position in the document as a bookmark end. |
| [EndColumnBookmark](endcolumnbookmark)(string) | Marks the current position in the document as a column bookmark end. The position must be in a table cell. |
| [EndEditableRange](endeditablerange)() | Marks the current position in the document as an editable range end. |
| [EndEditableRange](endeditablerange)(EditableRangeStart) | Marks the current position in the document as an editable range end. |
| [EndRow](endrow)() | Ends a table row in the document. |
| [EndTable](endtable)() | Ends a table in the document. |
| [InsertBreak](insertbreak)(BreakType) | Inserts a break of the specified type into the document. |
| [InsertCell](insertcell)() | Inserts a table cell into the document. |
| [InsertChart](insertchart)(ChartType, double, double) | Inserts an chart object into the document and scales it to the specified size. |
| [InsertChart](insertchart)(ChartType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserts an chart object into the document and scales it to the specified size. |
| [InsertCheckBox](insertcheckbox)(string, bool, int) | Inserts a checkbox form field at the current position. |
| [InsertCheckBox](insertcheckbox)(string, bool, bool, int) | Inserts a checkbox form field at the current position. |
| [InsertComboBox](insertcombobox)(string, string[], int) | Inserts a combobox form field at the current position. |
| [InsertDocument](insertdocument)(Document, ImportFormatMode) | Inserts a document at the cursor position. |
| [InsertDocument](insertdocument)(Document, ImportFormatMode, ImportFormatOptions) | Inserts a document at the cursor position. |
| [InsertField](insertfield)(string) | Inserts a Word field into a document and updates the field result. |
| [InsertField](insertfield)(FieldType, bool) | Inserts a Word field into a document and optionally updates the field result. |
| [InsertField](insertfield)(string, string) | Inserts a Word field into a document without updating the field result. |
| [InsertFootnote](insertfootnote)(FootnoteType, string) | Inserts a footnote or endnote into the document. |
| [InsertFootnote](insertfootnote)(FootnoteType, string, string) | Inserts a footnote or endnote into the document. |
| [InsertHorizontalRule](inserthorizontalrule)() | Inserts a horizontal rule shape into the document. |
| [InsertHtml](inserthtml)(string) | Inserts an HTML string into the document. |
| [InsertHtml](inserthtml)(string, bool) | Inserts an HTML string into the document. |
| [InsertHtml](inserthtml)(string, HtmlInsertOptions) | Inserts an HTML string into the document. Allows to specify additional options. |
| [InsertHyperlink](inserthyperlink)(string, string, bool) | Inserts a hyperlink into the document. |
| [InsertImage](insertimage)(byte[]) | Inserts an image from a byte array into the document. The image is inserted inline and at 100% scale. |
| [InsertImage](insertimage)(Image) | Inserts an image from a .NET Image object into the document. The image is inserted inline and at 100% scale. |
| [InsertImage](insertimage)(Stream) | Inserts an image from a stream into the document. The image is inserted inline and at 100% scale. |
| [InsertImage](insertimage)(string) | Inserts an image from a file or URL into the document. The image is inserted inline and at 100% scale. |
| [InsertImage](insertimage)(byte[], double, double) | Inserts an inline image from a byte array into the document and scales it to the specified size. |
| [InsertImage](insertimage)(Image, double, double) | Inserts an inline image from a .NET Image object into the document and scales it to the specified size. |
| [InsertImage](insertimage)(Stream, double, double) | Inserts an inline image from a stream into the document and scales it to the specified size. |
| [InsertImage](insertimage)(string, double, double) | Inserts an inline image from a file or URL into the document and scales it to the specified size. |
| [InsertImage](insertimage)(byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserts an image from a byte array at the specified position and size. |
| [InsertImage](insertimage)(Image, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserts an image from a .NET Image object at the specified position and size. |
| [InsertImage](insertimage)(Stream, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserts an image from a stream at the specified position and size. |
| [InsertImage](insertimage)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserts an image from a file or URL at the specified position and size. |
| [InsertNode](insertnode)(Node) | Inserts a text level node inside the current paragraph before the cursor. |
| [InsertOleObject](insertoleobject)(Stream, string, bool, Stream) | Inserts an embedded OLE object from a stream into the document. |
| [InsertOleObject](insertoleobject)(string, bool, bool, Stream) | Inserts an embedded or linked OLE object from a file into the document. Detects OLE object type using file extension. |
| [InsertOleObject](insertoleobject)(string, string, bool, bool, Stream) | Inserts an embedded or linked OLE object from a file into the document. Detects OLE object type using given progID parameter. |
| [InsertOleObjectAsIcon](insertoleobjectasicon)(Stream, string, string, string) | Inserts an embedded OLE object as icon from a stream into the document. Allows to specify icon file and caption. Detects OLE object type using given progID parameter. |
| [InsertOleObjectAsIcon](insertoleobjectasicon)(string, bool, string, string) | Inserts an embedded or linked OLE object as icon into the document. Allows to specify icon file and caption. Detects OLE object type using file extension. |
| [InsertOleObjectAsIcon](insertoleobjectasicon)(string, string, bool, string, string) | Inserts an embedded or linked OLE object as icon into the document. Allows to specify icon file and caption. Detects OLE object type using given progID parameter. |
| [InsertOnlineVideo](insertonlinevideo)(string, double, double) | Inserts an online video object into the document and scales it to the specified size. |
| [InsertOnlineVideo](insertonlinevideo)(string, string, byte[], double, double) | Inserts an online video object into the document and scales it to the specified size. |
| [InsertOnlineVideo](insertonlinevideo)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserts an online video object into the document and scales it to the specified size. |
| [InsertOnlineVideo](insertonlinevideo)(string, string, byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserts an online video object into the document and scales it to the specified size. |
| [InsertParagraph](insertparagraph)() | Inserts a paragraph break into the document. |
| [InsertShape](insertshape)(ShapeType, double, double) | Inserts inline shape with specified type and size. |
| [InsertShape](insertshape)(ShapeType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserts free-floating shape with specified position, size and text wrap type. |
| [InsertSignatureLine](insertsignatureline)(SignatureLineOptions) | Inserts a signature line at the current position. |
| [InsertSignatureLine](insertsignatureline)(SignatureLineOptions, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, WrapType) | Inserts a signature line at the specified position. |
| [InsertStyleSeparator](insertstyleseparator)() | Inserts style separator into the document. |
| [InsertTableOfContents](inserttableofcontents)(string) | Inserts a TOC (table of contents) field into the document. |
| [InsertTextInput](inserttextinput)(string, TextFormFieldType, string, string, int) | Inserts a text form field at the current position. |
| [MoveTo](moveto)(Node) | Moves the cursor to an inline node or to the end of a paragraph. |
| [MoveToBookmark](movetobookmark)(string) | Moves the cursor to a bookmark. |
| [MoveToBookmark](movetobookmark)(string, bool, bool) | Moves the cursor to a bookmark with greater precision. |
| [MoveToCell](movetocell)(int, int, int, int) | Moves the cursor to a table cell in the current section. |
| [MoveToDocumentEnd](movetodocumentend)() | Moves the cursor to the end of the document. |
| [MoveToDocumentStart](movetodocumentstart)() | Moves the cursor to the beginning of the document. |
| [MoveToField](movetofield)(Field, bool) | Moves the cursor to a field in the document. |
| [MoveToHeaderFooter](movetoheaderfooter)(HeaderFooterType) | Moves the cursor to the beginning of a header or footer in the current section. |
| [MoveToMergeField](movetomergefield)(string) | Moves the cursor to a position just beyond the specified merge field and removes the merge field. |
| [MoveToMergeField](movetomergefield)(string, bool, bool) | Moves the merge field to the specified merge field. |
| [MoveToParagraph](movetoparagraph)(int, int) | Moves the cursor to a paragraph in the current section. |
| [MoveToSection](movetosection)(int) | Moves the cursor to the beginning of the body in a specified section. |
| [PopFont](popfont)() | Retrieves character formatting previously saved on the stack. |
| [PushFont](pushfont)() | Saves current character formatting onto the stack. |
| [StartBookmark](startbookmark)(string) | Marks the current position in the document as a bookmark start. |
| [StartColumnBookmark](startcolumnbookmark)(string) | Marks the current position in the document as a column bookmark start. The position must be in a table cell. |
| [StartEditableRange](starteditablerange)() | Marks the current position in the document as an editable range start. |
| [StartTable](starttable)() | Starts a table in the document. |
| [Write](write)(string) | Inserts a string into the document at the current insert position. |
| [Writeln](writeln)() | Inserts a paragraph break into the document. |
| [Writeln](writeln)(string) | Inserts a string and a paragraph break into the document. |

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
