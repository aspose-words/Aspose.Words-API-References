---
title: PageInfo.GetSpecifiedPrinterPaperSource
linktitle: GetSpecifiedPrinterPaperSource
articleTitle: GetSpecifiedPrinterPaperSource
second_title: Aspose.Words för .NET
description: Upptäck GetSpecifiedPrinterPaperSource-metoden i PageInfo. Hämta effektivt den perfekta PaperSource-källan för sömlös utskrift av sidor.
type: docs
weight: 100
url: /sv/net/aspose.words.rendering/pageinfo/getspecifiedprinterpapersource/
---
## PageInfo.GetSpecifiedPrinterPaperSource method

HämtarPaperSource objekt lämpligt för utskrift sidan som representeras av detta[`PageInfo`](../) .

```csharp
public PaperSource GetSpecifiedPrinterPaperSource(PaperSourceCollection paperSources, 
    PaperSource defaultPageSettingsPaperSource)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| paperSources | PaperSourceCollection | Tillgängliga papperskällor. |
| defaultPageSettingsPaperSource | PaperSource | Papperskälla definierad i standardinställningarna för skrivaren. |

### Returvärde

Ett objekt som du kan använda i .NET-utskriftsramverket för att ange papperskällan.

## Anmärkningar

Den här metoden kräver .NET Framework 2.0 eller senare.

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

* class [PageInfo](../)
* namnutrymme [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* hopsättning [Aspose.Words](../../../)
