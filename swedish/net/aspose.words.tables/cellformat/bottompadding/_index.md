---
title: CellFormat.BottomPadding
linktitle: BottomPadding
articleTitle: BottomPadding
second_title: Aspose.Words för .NET
description: CellFormat BottomPadding fast egendom. Returnerar eller ställer in mängden utrymme i poäng som ska läggas till under innehållet i cellen i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.tables/cellformat/bottompadding/
---
## CellFormat.BottomPadding property

Returnerar eller ställer in mängden utrymme (i poäng) som ska läggas till under innehållet i cellen.

```csharp
public double BottomPadding { get; set; }
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
// Byggaren kommer att tillämpa dessa inställningar på sin nuvarande cell, och alla nya celler skapas efteråt.
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

// Den första cellen påverkades inte av utfyllnadsomställningen och har fortfarande standardvärdena.
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

// Den första cellen kommer fortfarande att växa i utdatadokumentet för att matcha storleken på dess närliggande cell.
doc.Save(ArtifactsDir + "DocumentBuilder.SetCellFormatting.docx");
```

### Se även

* class [CellFormat](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
