---
title: CellFormat Class
linktitle: CellFormat
articleTitle: CellFormat
second_title: Aspose.Words för .NET
description: Aspose.Words.Tables.CellFormat klass. Representerar all formatering för en tabellcell i C#.
type: docs
weight: 6260
url: /sv/net/aspose.words.tables/cellformat/
---
## CellFormat class

Representerar all formatering för en tabellcell.

För att lära dig mer, besök[Arbeta med tabeller](https://docs.aspose.com/words/net/working-with-tables/) dokumentationsartikel.

```csharp
public class CellFormat
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Borders](../../aspose.words.tables/cellformat/borders/) { get; } | Får samling av cellens kanter. |
| [BottomPadding](../../aspose.words.tables/cellformat/bottompadding/) { get; set; } | Returnerar eller ställer in mängden utrymme (i poäng) som ska läggas till under innehållet i cellen. |
| [FitText](../../aspose.words.tables/cellformat/fittext/) { get; set; } | Om`Sann` , passar text i cellen, komprimerar varje stycke till cellens bredd. |
| [HorizontalMerge](../../aspose.words.tables/cellformat/horizontalmerge/) { get; set; } | Anger hur cellen sammanfogas horisontellt med andra celler i raden. |
| [LeftPadding](../../aspose.words.tables/cellformat/leftpadding/) { get; set; } | Returnerar eller ställer in mängden utrymme (i poäng) som ska läggas till till vänster om innehållet i cellen. |
| [Orientation](../../aspose.words.tables/cellformat/orientation/) { get; set; } | Returnerar eller ställer in orienteringen för text i en tabellcell. |
| [PreferredWidth](../../aspose.words.tables/cellformat/preferredwidth/) { get; set; } | Returnerar eller ställer in önskad bredd på cellen. |
| [RightPadding](../../aspose.words.tables/cellformat/rightpadding/) { get; set; } | Returnerar eller ställer in mängden utrymme (i poäng) som ska läggas till till höger om innehållet i cellen. |
| [Shading](../../aspose.words.tables/cellformat/shading/) { get; } | Returnerar en[`Shading`](../../aspose.words/shading/) objekt som hänvisar till skuggformateringen för cellen. |
| [TopPadding](../../aspose.words.tables/cellformat/toppadding/) { get; set; } | Returnerar eller ställer in mängden utrymme (i poäng) som ska läggas till ovanför innehållet i cellen. |
| [VerticalAlignment](../../aspose.words.tables/cellformat/verticalalignment/) { get; set; } | Returnerar eller ställer in den vertikala justeringen av text i cellen. |
| [VerticalMerge](../../aspose.words.tables/cellformat/verticalmerge/) { get; set; } | Anger hur cellen sammanfogas med andra celler vertikalt. |
| [Width](../../aspose.words.tables/cellformat/width/) { get; set; } | Får cellens bredd i punkter. |
| [WrapText](../../aspose.words.tables/cellformat/wraptext/) { get; set; } | Om`Sann` , radbryt text för cellen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ClearFormatting](../../aspose.words.tables/cellformat/clearformatting/)() | Återställer till standardcellformatering. Ändrar inte cellens bredd. |
| [SetPaddings](../../aspose.words.tables/cellformat/setpaddings/)(*double, double, double, double*) | Ställer in mängden utrymme (i poäng) som ska läggas till till vänster/överst/höger/botten av innehållet i cellen. |

## Exempel

Visar hur man ändrar formateringen av en tabellcell.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

// Använd en cells "CellFormat"-egenskap för att ställa in formatering som ändrar cellens utseende.
firstCell.CellFormat.Width = 30;
firstCell.CellFormat.Orientation = TextOrientation.Downward;
firstCell.CellFormat.Shading.ForegroundPatternColor = Color.LightGreen;

doc.Save(ArtifactsDir + "Table.CellFormat.docx");
```

Visar hur du ändrar formatet för rader och celler i en tabell.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("City");
builder.InsertCell();
builder.Write("Country");
builder.EndRow();
builder.InsertCell();
builder.Write("London");
builder.InsertCell();
builder.Write("U.K.");
builder.EndTable();

// Använd den första radens "RowFormat"-egenskap för att ändra formateringen
// av innehållet i alla celler i den här raden.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Använd egenskapen "CellFormat" för den första cellen i den sista raden för att ändra formateringen av cellens innehåll.
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
```

Visar hur man bygger en tabell med anpassade ramar.

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

// Ändring av formateringen kommer att tillämpa den på den aktuella cellen,
// och eventuella nya celler som vi skapar med byggaren efteråt.
// Detta kommer inte att påverka cellerna som vi har lagt till tidigare.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Öka radhöjden så att den passar den vertikala texten.
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

* namnutrymme [Aspose.Words.Tables](../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../)
