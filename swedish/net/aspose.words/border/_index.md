---
title: Border Class
linktitle: Border
articleTitle: Border
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Border, din lösning för att anpassa objektkanter i dokument. Förbättra dina projekt med precision och stil!
type: docs
weight: 270
url: /sv/net/aspose.words/border/
---
## Border class

Representerar en kantlinje för ett objekt.

För att lära dig mer, besök[Programmering med dokument](https://docs.aspose.com/words/net/programming-with-documents/) dokumentationsartikel.

```csharp
public class Border : InternableComplexAttr
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Color](../../aspose.words/border/color/) { get; set; } | Hämtar eller ställer in kantfärgen. |
| [DistanceFromText](../../aspose.words/border/distancefromtext/) { get; set; } | Hämtar eller ställer in avståndet mellan kantlinjen och texten eller sidkanten i punkter. |
| [IsVisible](../../aspose.words/border/isvisible/) { get; } | Returer`sann` om den[`LineStyle`](./linestyle/) är inteNone . |
| [LineStyle](../../aspose.words/border/linestyle/) { get; set; } | Hämtar eller ställer in kantstilen. |
| [LineWidth](../../aspose.words/border/linewidth/) { get; set; } | Hämtar eller ställer in kantbredden i punkter. |
| [Shadow](../../aspose.words/border/shadow/) { get; set; } | Hämtar eller anger ett värde som anger om kanten har en skugga. |
| [ThemeColor](../../aspose.words/border/themecolor/) { get; set; } | Hämtar eller ställer in temafärgen i det tillämpade färgschemat som är associerat med detta Border-objekt. |
| [TintAndShade](../../aspose.words/border/tintandshade/) { get; set; } | Hämtar eller ställer in ett dubbelvärde som ljusar eller mörkar upp en färg. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ClearFormatting](../../aspose.words/border/clearformatting/)() | Återställer kantegenskaperna till standardvärdena. |
| [Equals](../../aspose.words/border/equals/#equals)(*Border*) | Avgör om den angivna ramen har samma värde som den aktuella ramen. |
| override [Equals](../../aspose.words/border/equals/#equals_1)(*object*) | Avgör om det angivna objektet har samma värde som det aktuella objektet. |
| override [GetHashCode](../../aspose.words/border/gethashcode/)() | Fungerar som en hashfunktion för den här typen. |

## Anmärkningar

Kantlinjer kan tillämpas på olika dokumentelement, inklusive stycke, textsekvens inuti ett stycke eller en tabellcell.

## Exempel

Visar hur man infogar en sträng omgiven av en kantlinje i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

Visar hur man infogar ett stycke med en övre kantlinje.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// Ställ endast in ThemeColor när LineWidth eller LineStyle är inställda.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Se även

* class [InternableComplexAttr](../internablecomplexattr/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
