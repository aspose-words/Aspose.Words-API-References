---
title: PageSet Class
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Saving.PageSet för effektiv dokumenthantering. Definiera enkelt slumpmässiga siduppsättningar och förbättra ditt arbetsflöde idag!
type: docs
weight: 6170
url: /sv/net/aspose.words.saving/pageset/
---
## PageSet class

Beskriver en slumpmässig uppsättning sidor.

För att lära dig mer, besök[Programmering med dokument](https://docs.aspose.com/words/net/programming-with-documents/) dokumentationsartikel.

```csharp
public sealed class PageSet : IEnumerable<int>
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [PageSet](pageset/#constructor_1)(*int*) | Skapar en uppsättning på en sida baserat på exakt sidindex. |
| [PageSet](pageset/#constructor_2)(*params int[]*) | Skapar en siduppsättning baserad på exakta sidindex. |
| [PageSet](pageset/#constructor)(*params PageRange[]*) | Skapar en siduppsättning baserad på intervall. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| static [All](../../aspose.words.saving/pageset/all/) { get; } | Hämtar en uppsättning med alla sidor i dokumentet i deras ursprungliga ordning. |
| static [Even](../../aspose.words.saving/pageset/even/) { get; } | Hämtar en uppsättning med alla jämna sidor i dokumentet i deras ursprungliga ordning. |
| static [Odd](../../aspose.words.saving/pageset/odd/) { get; } | Hämtar en uppsättning med alla udda sidor i dokumentet i deras ursprungliga ordning. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetEnumerator](../../aspose.words.saving/pageset/getenumerator/)() |  |

## Exempel

Visar hur man renderar en sida från ett dokument till en JPEG-bild.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Skapa ett "ImageSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att modifiera hur metoden renderar dokumentet till en bild.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
// Ställ in "PageSet" till "1" för att välja den andra sidan via
// det nollbaserade indexet att börja rendera dokumentet från.
options.PageSet = new PageSet(1);

// När vi sparar dokumentet i JPEG-format renderar Aspose.Words bara en sida.
// Den här bilden kommer att innehålla en sida med början från sida två,
// vilket bara kommer att vara den andra sidan i originaldokumentet.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
