---
title: BorderCollection.Left
linktitle: Left
articleTitle: Left
second_title: Aspose.Words för .NET
description: BorderCollection Left fast egendom. Får den vänstra kanten i C#.
type: docs
weight: 70
url: /sv/net/aspose.words/bordercollection/left/
---
## BorderCollection.Left property

Får den vänstra kanten.

```csharp
public Border Left { get; }
```

## Exempel

Visar hur man applicerar kant- och skuggfärg när man bygger ett bord.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Starta en tabell och ställ in en standardfärg/tjocklek för dess kanter.
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
// ställ in en anpassad kanttjocklek för alla nya celler skapade av byggaren,
// bygg sedan en andra rad.
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
