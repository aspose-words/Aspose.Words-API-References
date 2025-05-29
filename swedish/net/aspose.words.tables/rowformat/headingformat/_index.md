---
title: RowFormat.HeadingFormat
linktitle: HeadingFormat
articleTitle: HeadingFormat
second_title: Aspose.Words för .NET
description: Upptäck egenskapen RowFormat HeadingFormat och se till att dina tabellrubriker upprepas på varje sida för tydlighet och förbättrad läsbarhet i dokument med flera sidor.
type: docs
weight: 30
url: /sv/net/aspose.words.tables/rowformat/headingformat/
---
## RowFormat.HeadingFormat property

Sant om raden upprepas som tabellrubrik på varje sida när tabellen sträcker sig över mer än en sida.

```csharp
public bool HeadingFormat { get; set; }
```

## Exempel

Visar hur man bygger en tabell med rader som upprepas på varje sida.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();

// Alla rader som infogas medan flaggan "HeadingFormat" är satt till "true"
// kommer att visas högst upp i tabellen på varje sida den sträcker sig över.
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

// Lägg till tillräckligt många rader för att tabellen ska kunna sträcka sig över två sidor.
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
