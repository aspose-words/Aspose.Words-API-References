---
title: Class Border
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Border klass. Representerar en kant av ett objekt.
type: docs
weight: 80
url: /sv/net/aspose.words/border/
---
## Border class

Representerar en kant av ett objekt.

För att lära dig mer, besök[Programmering med dokument](https://docs.aspose.com/words/net/programming-with-documents/) dokumentationsartikel.

```csharp
public class Border : InternableComplexAttr
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Color](../../aspose.words/border/color/) { get; set; } | Hämtar eller ställer in kantfärgen. |
| [DistanceFromText](../../aspose.words/border/distancefromtext/) { get; set; } | Hämtar eller ställer in avståndet mellan kanten från text eller från sidkanten i punkter. |
| [IsVisible](../../aspose.words/border/isvisible/) { get; } | Returnerar`Sann` om[`LineStyle`](./linestyle/) är inteNone . |
| [LineStyle](../../aspose.words/border/linestyle/) { get; set; } | Hämtar eller ställer in kantstilen. |
| [LineWidth](../../aspose.words/border/linewidth/) { get; set; } | Hämtar eller ställer in kantbredden i punkter. |
| [Shadow](../../aspose.words/border/shadow/) { get; set; } | Hämtar eller ställer in ett värde som anger om gränsen har en skugga. |
| [ThemeColor](../../aspose.words/border/themecolor/) { get; set; } | Hämtar eller ställer in temafärgen i det tillämpade färgschemat som är associerat med detta Border-objekt. |
| [TintAndShade](../../aspose.words/border/tintandshade/) { get; set; } | Hämtar eller ställer in ett dubbelt värde som gör en färg ljusare eller mörkare. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ClearFormatting](../../aspose.words/border/clearformatting/)() | Återställer gränsegenskaper till standardvärden. |
| [Equals](../../aspose.words/border/equals/#equals)(Border) | Bestämmer om den angivna gränsen är lika i värde med den aktuella gränsen. |
| override [Equals](../../aspose.words/border/equals/#equals_1)(object) | Bestämmer om det angivna objektet har samma värde som det aktuella objektet. |
| override [GetHashCode](../../aspose.words/border/gethashcode/)() | Fungerar som en hashfunktion för denna typ. |

### Anmärkningar

Kanter kan appliceras på olika dokumentelement inklusive stycke, textkörning inuti ett stycke eller en tabellcell.

### Exempel

Visar hur man infogar en sträng omgiven av en kant i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

Visar hur man infogar ett stycke med en övre kant.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// Ställ in ThemeColor endast när LineWidth eller LineStyle är inställda.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Se även

* class [InternableComplexAttr](../internablecomplexattr/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)


