---
title: DocumentBuilder.InsertCell
linktitle: InsertCell
articleTitle: InsertCell
second_title: Aspose.Words för .NET
description: Förbättra dina dokument enkelt med DocumentBuilder InsertCell-metoden – lägg snabbt till anpassningsbara tabellceller för förbättrad organisation och tydlighet.
type: docs
weight: 270
url: /sv/net/aspose.words/documentbuilder/insertcell/
---
## DocumentBuilder.InsertCell method

Infogar en tabellcell i dokumentet.

```csharp
public Cell InsertCell()
```

### Returvärde

Cellnoden som just infogades.

## Anmärkningar

För att starta ett bord, ring bara`InsertCell` Efter detta kommer allt innehåll du lägger till med hjälp av andra metoder i[`DocumentBuilder`](../) klassen kommer att läggas till i den aktuella cellen.

För att starta en ny cell i samma rad, anropa`InsertCell` igen.

För att avsluta ett anrop av en tabellrad[`EndRow`](../endrow/).

Använd[`CellFormat`](../cellformat/) egenskap för att ange cellformatering.

## Exempel

Visar hur man använder en dokumentbyggare för att skapa en tabell.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Starta tabellen och fyll sedan den första raden med två celler.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

// Anropa byggarens "EndRow"-metod för att starta en ny rad.
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateTable.docx");
```

Visar hur man skapar en tabell med anpassade ramar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Ställa in tabellformateringsalternativ för en dokumentbyggare
// kommer att tillämpa dem på varje rad och cell som vi lägger till med den.
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

// Ändring av formateringen kommer att tillämpas på den aktuella cellen,
// och alla nya celler som vi skapar med byggaren efteråt.
// Detta kommer inte att påverka de celler som vi har lagt till tidigare.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Öka radhöjden för att få plats med den vertikala texten.
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

### Se även

* class [Cell](../../../aspose.words.tables/cell/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
