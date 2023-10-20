---
title: RowFormat.HeadingFormat
linktitle: HeadingFormat
articleTitle: HeadingFormat
second_title: Aspose.Words för .NET
description: RowFormat HeadingFormat fast egendom. Sant om raden upprepas som en tabellrubrik på varje sida när tabellen sträcker sig över mer än en sida i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.tables/rowformat/headingformat/
---
## RowFormat.HeadingFormat property

Sant om raden upprepas som en tabellrubrik på varje sida när tabellen sträcker sig över mer än en sida.

```csharp
public bool HeadingFormat { get; set; }
```

## Exempel

Visar hur man bygger en tabell med rader som upprepas på varje sida.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();

// Alla rader infogade medan "HeadingFormat"-flaggan är inställd på "true"
// kommer att dyka upp överst i tabellen på varje sida som den sträcker sig över.
builder.RowFormat.HeadingFormat = true;
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.CellFormat.Width = 100;
builder.InsertCell();
builder.Write("Heading row 1");
builder.EndRow();
builder.InsertCell();
builder.Write("Heading row 2");
builder.EndRow();

builder.CellFormat.Width = 50;
builder.ParagraphFormat.ClearFormatting();
builder.RowFormat.HeadingFormat = false;

// Lägg till tillräckligt många rader för att tabellen ska sträcka sig över två sidor.
for (int i = 0; i < 50; i++)
{
    builder.InsertCell();
    builder.Write($"Row {table.Rows.Count}, column 1.");
    builder.InsertCell();
    builder.Write($"Row {table.Rows.Count}, column 2.");
    builder.EndRow();
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableSetHeadingRow.docx");
```

### Se även

* class [RowFormat](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
