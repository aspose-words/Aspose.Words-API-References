---
title: BorderCollection.Bottom
linktitle: Bottom
articleTitle: Bottom
second_title: Aspose.Words för .NET
description: Upptäck egenskapen BorderCollection Bottom för att enkelt komma åt och anpassa din nedre kantlinje för ökad designflexibilitet och stil.
type: docs
weight: 10
url: /sv/net/aspose.words/bordercollection/bottom/
---
## BorderCollection.Bottom property

Hämtar den nedre kanten.

```csharp
public Border Bottom { get; }
```

## Exempel

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

* class [Border](../../border/)
* class [BorderCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
