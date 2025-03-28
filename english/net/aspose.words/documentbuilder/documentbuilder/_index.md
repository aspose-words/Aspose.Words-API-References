---
title: DocumentBuilder
linktitle: DocumentBuilder
articleTitle: DocumentBuilder
second_title: Aspose.Words for .NET
description: Create powerful documents effortlessly with DocumentBuilder. Initialize a new instance and streamline your document management today!
type: docs
weight: 10
url: /net/aspose.words/documentbuilder/documentbuilder/
---
## DocumentBuilder() {#constructor}

Initializes a new instance of this class.

```csharp
public DocumentBuilder()
```

## Remarks

Creates a new [`DocumentBuilder`](../) object and attaches it to a new [`Document`](../../document/) object.

## Examples

Shows how to insert formatted text using DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Specify font formatting, then add text.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### See Also

* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## DocumentBuilder(*[DocumentBuilderOptions](../../documentbuilderoptions/)*) {#constructor_3}

Initializes a new instance of this class.

```csharp
public DocumentBuilder(DocumentBuilderOptions options)
```

## Remarks

Creates a new [`DocumentBuilder`](../) object and attaches it to a new [`Document`](../../document/) object. Additional document building options can be specified.

## Examples

Shows how to ignore table formatting for content after.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Adds content before the table.
// Default font size is 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Changes the font size inside the table.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// If ContextTableFormatting is true, then table formatting isn't applied to the content after.
// If ContextTableFormatting is false, then table formatting is applied to the content after.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### See Also

* class [DocumentBuilderOptions](../../documentbuilderoptions/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## DocumentBuilder(*[Document](../../document/)*) {#constructor_1}

Initializes a new instance of this class.

```csharp
public DocumentBuilder(Document doc)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | Document | The [`Document`](../../document/) object to attach to. |

## Remarks

Creates a new [`DocumentBuilder`](../) object, attaches to the specified [`Document`](../../document/) object. The cursor is positioned at the beginning of the document.

## Examples

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

Shows how to insert a Table of contents (TOC) into a document using heading styles as entries.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a table of contents for the first page of the document.
// Configure the table to pick up paragraphs with headings of levels 1 to 3.
// Also, set its entries to be hyperlinks that will take us
// to the location of the heading when left-clicked in Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Populate the table of contents by adding paragraphs with heading styles.
// Each such heading with a level between 1 and 3 will create an entry in the table.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// A table of contents is a field of a type that needs to be updated to show an up-to-date result.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### See Also

* class [Document](../../document/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## DocumentBuilder(*[Document](../../document/), [DocumentBuilderOptions](../../documentbuilderoptions/)*) {#constructor_2}

Initializes a new instance of this class.

```csharp
public DocumentBuilder(Document doc, DocumentBuilderOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | Document | The [`Document`](../../document/) object to attach to. |
| options | DocumentBuilderOptions | Additional options for the document building process. |

## Remarks

Creates a new [`DocumentBuilder`](../) object, attaches to the specified [`Document`](../../document/) object. The cursor is positioned at the beginning of the document.

## Examples

Shows how to ignore table formatting for content after.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Adds content before the table.
// Default font size is 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Changes the font size inside the table.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// If ContextTableFormatting is true, then table formatting isn't applied to the content after.
// If ContextTableFormatting is false, then table formatting is applied to the content after.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### See Also

* class [Document](../../document/)
* class [DocumentBuilderOptions](../../documentbuilderoptions/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
