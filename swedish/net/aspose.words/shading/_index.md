---
title: Shading Class
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Shading, utformad för att förbättra dina dokument med anpassningsbara skuggningsattribut för ett professionellt utseende.
type: docs
weight: 6820
url: /sv/net/aspose.words/shading/
---
## Shading class

Innehåller skuggningsattribut för ett objekt.

För att lära dig mer, besök[Programmering med dokument](https://docs.aspose.com/words/net/programming-with-documents/) dokumentationsartikel.

```csharp
public class Shading : InternableComplexAttr
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BackgroundPatternColor](../../aspose.words/shading/backgroundpatterncolor/) { get; set; } | Hämtar eller ställer in färgen som tillämpas på bakgrunden av`Shading` objekt. |
| [BackgroundPatternThemeColor](../../aspose.words/shading/backgroundpatternthemecolor/) { get; set; } | Hämtar eller ställer in bakgrundsmönstrets temafärg i det tillämpade färgschemat som är associerat med detta`Shading` objekt. |
| [BackgroundTintAndShade](../../aspose.words/shading/backgroundtintandshade/) { get; set; } | Hämtar eller ställer in ett dubbelvärde som ljusar eller mörkar upp en bakgrundstemafärg. |
| [ForegroundPatternColor](../../aspose.words/shading/foregroundpatterncolor/) { get; set; } | Hämtar eller ställer in färgen som tillämpas på förgrunden av`Shading` objekt. |
| [ForegroundPatternThemeColor](../../aspose.words/shading/foregroundpatternthemecolor/) { get; set; } | Hämtar eller ställer in temafärgen för förgrundsmönstret i det tillämpade färgschemat som är associerat med detta`Shading` objekt. |
| [ForegroundTintAndShade](../../aspose.words/shading/foregroundtintandshade/) { get; set; } | Hämtar eller ställer in ett dubbelvärde som ljusar eller mörkar upp en förgrundstemafärg. |
| [Texture](../../aspose.words/shading/texture/) { get; set; } | Hämtar eller ställer in skuggningstexturen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ClearFormatting](../../aspose.words/shading/clearformatting/)() | Tar bort skuggning från objektet. |
| override [Equals](../../aspose.words/shading/equals/#equals_1)(*object*) | Avgör om det angivna objektet har samma värde som det aktuella objektet. |
| [Equals](../../aspose.words/shading/equals/#equals)(*Shading*) | Avgör om den angivna`Shading` är lika värdefullt som den nuvarande`Shading` . |
| override [GetHashCode](../../aspose.words/shading/gethashcode/)() | Fungerar som en hashfunktion för den här typen. |

## Exempel

Visar hur man dekorerar text med ramar och skuggning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

BorderCollection borders = builder.ParagraphFormat.Borders;
borders.DistanceFromText = 20;
borders[BorderType.Left].LineStyle = LineStyle.Double;
borders[BorderType.Right].LineStyle = LineStyle.Double;
borders[BorderType.Top].LineStyle = LineStyle.Double;
borders[BorderType.Bottom].LineStyle = LineStyle.Double;

Shading shading = builder.ParagraphFormat.Shading;
shading.Texture = TextureIndex.TextureDiagonalCross;
shading.BackgroundPatternColor = Color.LightCoral;
shading.ForegroundPatternColor = Color.LightSalmon;

builder.Write("This paragraph is formatted with a double border and shading.");
doc.Save(ArtifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
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

* class [InternableComplexAttr](../internablecomplexattr/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
