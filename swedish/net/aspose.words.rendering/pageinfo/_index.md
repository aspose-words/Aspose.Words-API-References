---
title: PageInfo Class
linktitle: PageInfo
articleTitle: PageInfo
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Rendering.PageInfo, som ger viktig information om varje dokumentsida och förbättrar din dokumentrenderingsupplevelse.
type: docs
weight: 5300
url: /sv/net/aspose.words.rendering/pageinfo/
---
## PageInfo class

Representerar information om en viss dokumentsida.

För att lära dig mer, besök[Tolkning](https://docs.aspose.com/words/net/rendering/) dokumentationsartikel.

```csharp
public class PageInfo
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Colored](../../aspose.words.rendering/pageinfo/colored/) { get; } | Returer`sann` om sidan innehåller färgat innehåll. |
| [HeightInPoints](../../aspose.words.rendering/pageinfo/heightinpoints/) { get; } | Hämtar sidans höjd i punkter. |
| [Landscape](../../aspose.words.rendering/pageinfo/landscape/) { get; } | Returer`sann` om sidorienteringen som anges i dokumentet för den här sidan är liggande. |
| [PaperSize](../../aspose.words.rendering/pageinfo/papersize/) { get; } | Hämtar pappersstorleken som uppräkning. |
| [PaperTray](../../aspose.words.rendering/pageinfo/papertray/) { get; } | Hämtar pappersfacket (facket) för den här sidan enligt specifikationen i dokumentet. Värdet är implementeringsspecifikt (skrivarspecifikt). |
| [SizeInPoints](../../aspose.words.rendering/pageinfo/sizeinpoints/) { get; } | Hämtar sidstorleken i punkter. |
| [WidthInPoints](../../aspose.words.rendering/pageinfo/widthinpoints/) { get; } | Hämtar sidans bredd i punkter. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetDotNetPaperSize](../../aspose.words.rendering/pageinfo/getdotnetpapersize/)(*PaperSizeCollection*) | HämtarPaperSize objekt lämpligt för utskrift sidan som representeras av detta`PageInfo` . |
| [GetSizeInPixels](../../aspose.words.rendering/pageinfo/getsizeinpixels/#getsizeinpixels)(*float, float*) | Beräknar sidstorleken i pixlar för en angiven zoomfaktor och upplösning. |
| [GetSizeInPixels](../../aspose.words.rendering/pageinfo/getsizeinpixels/#getsizeinpixels_1)(*float, float, float*) | Beräknar sidstorleken i pixlar för en angiven zoomfaktor och upplösning. |
| [GetSpecifiedPrinterPaperSource](../../aspose.words.rendering/pageinfo/getspecifiedprinterpapersource/)(*PaperSourceCollection, PaperSource*) | HämtarPaperSource objekt lämpligt för utskrift sidan som representeras av detta`PageInfo` . |

## Anmärkningar

Sidbredden och -höjden som returneras av detta objekt representerar sidans "slutliga" storlek, t.ex. de är redan roterade till rätt orientering.

## Exempel

Visar hur man skriver ut information om sidstorlek och orientering för varje sida i ett Word-dokument.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Det första avsnittet har två sidor. Vi kommer att tilldela ett annat pappersfack till varje sida,
// vars nummer matchar en typ av papperskälla. Dessa källor och deras typer kommer att variera
// beroende på den installerade skrivardrivrutinen.
PrinterSettings.PaperSourceCollection paperSources = new PrinterSettings().PaperSources;

doc.FirstSection.PageSetup.FirstPageTray = paperSources[0].RawKind;
doc.FirstSection.PageSetup.OtherPagesTray = paperSources[1].RawKind;

Console.WriteLine("Document \"{0}\" contains {1} pages.", doc.OriginalFileName, doc.PageCount);

float scale = 1.0f;
float dpi = 96;

for (int i = 0; i < doc.PageCount; i++)
{
    // Varje sida har ett PageInfo-objekt, vars index är respektive sidas nummer.
    PageInfo pageInfo = doc.GetPageInfo(i);

    // Skriv ut sidans orientering och mått.
    Console.WriteLine($"Page {i + 1}:");
    Console.WriteLine($"\tOrientation:\t{(pageInfo.Landscape ? "Landscape" : "Portrait")}");
    Console.WriteLine($"\tPaper size:\t\t{pageInfo.PaperSize} ({pageInfo.WidthInPoints:F0}x{pageInfo.HeightInPoints:F0}pt)");
    Console.WriteLine($"\tSize in points:\t{pageInfo.SizeInPoints}");
    Console.WriteLine($"\tSize in pixels:\t{pageInfo.GetSizeInPixels(1.0f, 96)} at {scale * 100}% scale, {dpi} dpi");

    // Skriv ut informationen om källfacket.
    Console.WriteLine($"\tTray:\t{pageInfo.PaperTray}");
    PaperSource source = pageInfo.GetSpecifiedPrinterPaperSource(paperSources, paperSources[0]);
    Console.WriteLine($"\tSuitable print source:\t{source.SourceName}, kind: {source.Kind}");
}
```

### Se även

* namnutrymme [Aspose.Words.Rendering](../../aspose.words.rendering/)
* hopsättning [Aspose.Words](../../)
