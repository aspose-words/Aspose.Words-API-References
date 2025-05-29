---
title: DocumentBuilder.EndRow
linktitle: EndRow
articleTitle: EndRow
second_title: Aspose.Words för .NET
description: Avsluta enkelt tabellrader i dina dokument med DocumentBuilders EndRow-metod. Effektivisera din formatering och förbättra dokumentets tydlighet!
type: docs
weight: 240
url: /sv/net/aspose.words/documentbuilder/endrow/
---
## DocumentBuilder.EndRow method

Avslutar en tabellrad i dokumentet.

```csharp
public Row EndRow()
```

### Returvärde

Radnoden som just blev klar.

## Anmärkningar

Samtal`EndRow` för att avsluta en tabellrad. Om du anropar[`InsertCell`](../insertcell/) immediately efter det, sedan fortsätter tabellen på en ny rad.

Använd[`RowFormat`](../rowformat/) egenskap för att ange radformatering.

## Exempel

Visar hur man sammanfogar tabellceller vertikalt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en cell i den första kolumnen på den första raden.
// Den här cellen blir den första i ett intervall av vertikalt sammanfogade celler.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// Infoga en cell i den andra kolumnen på den första raden och avsluta sedan raden.
// Konfigurera även byggaren för att inaktivera vertikal sammanslagning i skapade celler.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();

 // Infoga en cell i den första kolumnen på den andra raden.
// Istället för att lägga till textinnehåll kommer vi att sammanfoga den här cellen med den första cellen som vi lade till direkt ovanför.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.Previous;

// Infoga ytterligare en oberoende cell i den andra kolumnen på den andra raden.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.VerticalMerge.docx");
```

Visar hur man bygger en formaterad 2x2-tabell.

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

// När tabellen skapas kommer dokumentbyggaren att tillämpa dess aktuella RowFormat/CellFormat-egenskapsvärden
// till den aktuella raden/cellen där markören befinner sig och alla nya rader/celler allt eftersom de skapas.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

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

// Tidigare tillagda rader och celler påverkas inte retroaktivt av ändringar i formateringen i verktyget.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
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

* class [Row](../../../aspose.words.tables/row/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
