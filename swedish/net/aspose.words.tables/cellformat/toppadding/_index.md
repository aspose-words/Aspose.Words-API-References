---
title: CellFormat.TopPadding
linktitle: TopPadding
articleTitle: TopPadding
second_title: Aspose.Words för .NET
description: Upptäck egenskapen CellFormat TopPadding för att anpassa avståndet ovanför cellinnehållet i punkter, vilket förbättrar kalkylbladets layout och läsbarhet.
type: docs
weight: 110
url: /sv/net/aspose.words.tables/cellformat/toppadding/
---
## CellFormat.TopPadding property

Returnerar eller anger mängden utrymme (i punkter) som ska läggas till ovanför cellens innehåll.

```csharp
public double TopPadding { get; set; }
```

## Exempel

Visar hur man formaterar celler med en dokumentbyggare.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Infoga en andra cell och konfigurera sedan utfyllnadsalternativ för celltext.
// Skaparen kommer att tillämpa dessa inställningar på sin nuvarande cell, och alla nya celler skapas efteråt.
builder.InsertCell();

CellFormat cellFormat = builder.CellFormat;
cellFormat.Width = 250;
cellFormat.LeftPadding = 30;
cellFormat.RightPadding = 30;
cellFormat.TopPadding = 30;
cellFormat.BottomPadding = 30;

builder.Write("Row 1, cell 2.");
builder.EndRow();
builder.EndTable();

// Den första cellen påverkades inte av omkonfigureringen av utfyllnaden och innehåller fortfarande standardvärdena.
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.Width);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.LeftPadding);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.RightPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.TopPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.BottomPadding);

Assert.AreEqual(250.0d, table.FirstRow.Cells[1].CellFormat.Width);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.LeftPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.RightPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.TopPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.BottomPadding);

// Den första cellen kommer fortfarande att växa i utdatadokumentet för att matcha storleken på dess angränsande cell.
doc.Save(ArtifactsDir + "DocumentBuilder.SetCellFormatting.docx");
```

### Se även

* class [CellFormat](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
