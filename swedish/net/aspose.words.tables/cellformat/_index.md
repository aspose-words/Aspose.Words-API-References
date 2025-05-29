---
title: CellFormat Class
linktitle: CellFormat
articleTitle: CellFormat
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Tables.CellFormat för omfattande formatering av tabellceller. Förbättra din dokumentformatering med lättanvända funktioner!
type: docs
weight: 7110
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
| [Borders](../../aspose.words.tables/cellformat/borders/) { get; } | Hämtar en samling av cellens kantlinjer. |
| [BottomPadding](../../aspose.words.tables/cellformat/bottompadding/) { get; set; } | Returnerar eller anger mängden mellanslag (i punkter) som ska läggas till under cellens innehåll. |
| [FitText](../../aspose.words.tables/cellformat/fittext/) { get; set; } | Om`sann` , anpassar texten i cellen och komprimerar varje stycke till cellens bredd. |
| [HideMark](../../aspose.words.tables/cellformat/hidemark/) { get; set; } | Returnerar eller anger synligheten för cellmarkeringen. |
| [HorizontalMerge](../../aspose.words.tables/cellformat/horizontalmerge/) { get; set; } | Anger hur cellen sammanfogas horisontellt med andra celler i raden. |
| [LeftPadding](../../aspose.words.tables/cellformat/leftpadding/) { get; set; } | Returnerar eller anger mängden utrymme (i punkter) som ska läggas till vänster om cellens innehåll. |
| [Orientation](../../aspose.words.tables/cellformat/orientation/) { get; set; } | Returnerar eller anger orienteringen för text i en tabellcell. |
| [PreferredWidth](../../aspose.words.tables/cellformat/preferredwidth/) { get; set; } | Returnerar eller anger önskad cellbredd. |
| [RightPadding](../../aspose.words.tables/cellformat/rightpadding/) { get; set; } | Returnerar eller anger mängden utrymme (i punkter) som ska läggas till till höger om cellens innehåll. |
| [Shading](../../aspose.words.tables/cellformat/shading/) { get; } | Returnerar en[`Shading`](../../aspose.words/shading/) objekt som refererar till skuggningsformateringen för cellen. |
| [TopPadding](../../aspose.words.tables/cellformat/toppadding/) { get; set; } | Returnerar eller anger mängden utrymme (i punkter) som ska läggas till ovanför cellens innehåll. |
| [VerticalAlignment](../../aspose.words.tables/cellformat/verticalalignment/) { get; set; } | Returnerar eller anger den vertikala justeringen av text i cellen. |
| [VerticalMerge](../../aspose.words.tables/cellformat/verticalmerge/) { get; set; } | Anger hur cellen sammanfogas med andra celler vertikalt. |
| [Width](../../aspose.words.tables/cellformat/width/) { get; set; } | Hämtar cellens bredd i punkter. |
| [WrapText](../../aspose.words.tables/cellformat/wraptext/) { get; set; } | Om`sann` , radbryt text för cellen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ClearFormatting](../../aspose.words.tables/cellformat/clearformatting/)() | Återställer till standardcellformatering. Ändrar inte cellens bredd. |
| [SetPaddings](../../aspose.words.tables/cellformat/setpaddings/)(*double, double, double, double*) | Anger mängden utrymme (i punkter) som ska läggas till vänster/överst/höger/nederst i cellens innehåll. |

## Exempel

Visar hur man ändrar formateringen av en tabellcell.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

// Använd en cells "CellFormat"-egenskap för att ange formatering som ändrar cellens utseende.
firstCell.CellFormat.Width = 30;
firstCell.CellFormat.Orientation = TextOrientation.Downward;
firstCell.CellFormat.Shading.ForegroundPatternColor = Color.LightGreen;

doc.Save(ArtifactsDir + "Table.CellFormat.docx");
```

Visar hur man ändrar formatet för rader och celler i en tabell.

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
// av innehållet i alla celler på den här raden.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Använd egenskapen "CellFormat" för den första cellen på den sista raden för att ändra formateringen av cellens innehåll.
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
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

* namnutrymme [Aspose.Words.Tables](../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../)
