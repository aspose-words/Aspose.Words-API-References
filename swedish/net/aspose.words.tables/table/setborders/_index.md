---
title: Table.SetBorders
linktitle: SetBorders
articleTitle: SetBorders
second_title: Aspose.Words för .NET
description: Anpassa dina tabeller enkelt med SetBorders-metoden och justera linjestil, bredd och färg för ett elegant och professionellt utseende.
type: docs
weight: 440
url: /sv/net/aspose.words.tables/table/setborders/
---
## Table.SetBorders method

Ställer in alla tabellkanter till angiven linjestil, bredd och färg.

```csharp
public void SetBorders(LineStyle lineStyle, double lineWidth, Color color)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| lineStyle | LineStyle | Linjestilen som ska tillämpas. |
| lineWidth | Double | Linjebredden som ska ställas in (i punkter). |
| color | Color | Färgen som ska användas för kanten. |

## Exempel

Visar hur man formaterar alla en tabells kantlinjer samtidigt.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Rensa alla befintliga ramar från tabellen.
table.ClearBorders();

// Ställ in en enda grön linje som ska fungera som varje yttre och inre kantlinje för den här tabellen.
table.SetBorders(LineStyle.Single, 1.5, Color.Green);

doc.Save(ArtifactsDir + "Table.SetBorders.docx");
```

Visar hur man använder kant- och skuggningsfärg när man skapar en tabell.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Starta en tabell och ange en standardfärg/tjocklek för dess kanter.
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// Skapa en rad med två celler med olika bakgrundsfärger.
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// Återställ cellformateringen för att inaktivera bakgrundsfärgerna
// ange en anpassad kanttjocklek för alla nya celler som skapas av byggaren,
// sedan bygga en andra rad.
builder.CellFormat.ClearFormatting();
builder.CellFormat.Borders.Left.LineWidth = 4.0;
builder.CellFormat.Borders.Right.LineWidth = 4.0;
builder.CellFormat.Borders.Top.LineWidth = 4.0;
builder.CellFormat.Borders.Bottom.LineWidth = 4.0;

builder.InsertCell();
builder.Writeln("Row 2, Cell 1.");
builder.InsertCell();
builder.Writeln("Row 2, Cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.TableBordersAndShading.docx");
```

### Se även

* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
