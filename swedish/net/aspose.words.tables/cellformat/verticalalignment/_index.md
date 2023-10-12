---
title: CellFormat.VerticalAlignment
second_title: Aspose.Words för .NET API Referens
description: CellFormat fast egendom. Returnerar eller ställer in den vertikala justeringen av text i cellen.
type: docs
weight: 120
url: /sv/net/aspose.words.tables/cellformat/verticalalignment/
---
## CellFormat.VerticalAlignment property

Returnerar eller ställer in den vertikala justeringen av text i cellen.

```csharp
public CellVerticalAlignment VerticalAlignment { get; set; }
```

### Exempel

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

* enum [CellVerticalAlignment](../../cellverticalalignment/)
* class [CellFormat](../)
* namnutrymme [Aspose.Words.Tables](../../cellformat/)
* hopsättning [Aspose.Words](../../../)


