---
title: BorderCollection Class
linktitle: BorderCollection
articleTitle: BorderCollection
second_title: Aspose.Words för .NET
description: Utforska Aspose.Words.BorderCollection, din lösning för att enkelt hantera och anpassa kantobjekt för förbättrad dokumentformatering.
type: docs
weight: 280
url: /sv/net/aspose.words/bordercollection/
---
## BorderCollection class

En samling av[`Border`](../border/) objekt.

För att lära dig mer, besök[Programmering med dokument](https://docs.aspose.com/words/net/programming-with-documents/) dokumentationsartikel.

```csharp
public sealed class BorderCollection : IEnumerable<Border>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Bottom](../../aspose.words/bordercollection/bottom/) { get; } | Hämtar den nedre kanten. |
| [Color](../../aspose.words/bordercollection/color/) { get; set; } | Hämtar eller ställer in kantfärgen. |
| [Count](../../aspose.words/bordercollection/count/) { get; } | Hämtar antalet ramar i samlingen. |
| [DistanceFromText](../../aspose.words/bordercollection/distancefromtext/) { get; set; } | Hämtar eller ställer in avståndet mellan kantlinjen och texten i punkter. |
| [Horizontal](../../aspose.words/bordercollection/horizontal/) { get; } | Hämtar den horisontella kantlinjen som används mellan celler eller överensstämmande stycken. |
| [Item](../../aspose.words/bordercollection/item/) { get; } | Hämtar en[`Border`](../border/) objekt efter kanttyp. (2 indexers) |
| [Left](../../aspose.words/bordercollection/left/) { get; } | Hämtar den vänstra kanten. |
| [LineStyle](../../aspose.words/bordercollection/linestyle/) { get; set; } | Hämtar eller ställer in kantstilen. |
| [LineWidth](../../aspose.words/bordercollection/linewidth/) { get; set; } | Hämtar eller ställer in kantbredden i punkter. |
| [Right](../../aspose.words/bordercollection/right/) { get; } | Hämtar rätt kantlinje. |
| [Shadow](../../aspose.words/bordercollection/shadow/) { get; set; } | Hämtar eller anger ett värde som anger om kanten har en skugga. |
| [Top](../../aspose.words/bordercollection/top/) { get; } | Hämtar den övre kanten. |
| [Vertical](../../aspose.words/bordercollection/vertical/) { get; } | Hämtar den vertikala kantlinjen som används mellan celler. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ClearFormatting](../../aspose.words/bordercollection/clearformatting/)() | Tar bort alla kanter för ett objekt. |
| [Equals](../../aspose.words/bordercollection/equals/#equals)(*BorderCollection*) | Jämför samlingar av ramar. |
| [GetEnumerator](../../aspose.words/bordercollection/getenumerator/)() | Returnerar ett uppräknarobjekt som kan användas för att iterera över alla gränser i samlingen. |

## Anmärkningar

Olika dokumentelement har olika ramar. Till exempel,[`ParagraphFormat`](../paragraphformat/) har[`Bottom`](./bottom/) ,[`Left`](./left/) ,[`Right`](./right/) och[`Top`](./top/) borders. Du kan ange olika formateringar för varje kant oberoende av varandra eller räkna upp alla kantlinjer och tillämpa samma formatering.

## Exempel

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

* class [Border](../border/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
