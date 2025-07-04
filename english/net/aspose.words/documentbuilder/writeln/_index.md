---
title: DocumentBuilder.Writeln
linktitle: Writeln
articleTitle: Writeln
second_title: Aspose.Words for .NET
description: Enhance your documents effortlessly with DocumentBuilder's Writeln method—insert text and paragraph breaks seamlessly for improved readability.
type: docs
weight: 700
url: /net/aspose.words/documentbuilder/writeln/
---
## Writeln(*string*) {#writeln_1}

Inserts a string and a paragraph break into the document.

```csharp
public void Writeln(string text)
```

| Parameter | Type | Description |
| --- | --- | --- |
| text | String | The string to insert into the document. |

## Remarks

Current font and paragraph formatting specified by the [`Font`](../font/) and [`ParagraphFormat`](../paragraphformat/) properties are used.

## Examples

Shows how to build a formatted 2x2 table.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// While building the table, the document builder will apply its current RowFormat/CellFormat property values
// to the current row/cell that its cursor is in and any new rows/cells as it creates them.
Assert.That(table.Rows[0].Cells[0].CellFormat.VerticalAlignment, Is.EqualTo(CellVerticalAlignment.Center));
Assert.That(table.Rows[0].Cells[1].CellFormat.VerticalAlignment, Is.EqualTo(CellVerticalAlignment.Center));

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
Assert.That(table.Rows[0].RowFormat.Height, Is.EqualTo(0));
Assert.That(table.Rows[0].RowFormat.HeightRule, Is.EqualTo(HeightRule.Auto));
Assert.That(table.Rows[1].RowFormat.Height, Is.EqualTo(100));
Assert.That(table.Rows[1].RowFormat.HeightRule, Is.EqualTo(HeightRule.Exactly));
Assert.That(table.Rows[1].Cells[0].CellFormat.Orientation, Is.EqualTo(TextOrientation.Upward));
Assert.That(table.Rows[1].Cells[1].CellFormat.Orientation, Is.EqualTo(TextOrientation.Downward));

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

### See Also

* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## Writeln() {#writeln}

Inserts a paragraph break into the document.

```csharp
public void Writeln()
```

## Remarks

Calls [`InsertParagraph`](../insertparagraph/).

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

### See Also

* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
