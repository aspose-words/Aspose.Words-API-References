---
title: PageInfo.GetSizeInPixels
linktitle: GetSizeInPixels
articleTitle: GetSizeInPixels
second_title: Aspose.Words för .NET
description: Upptäck PageInfo GetSizeInPixels-metoden för att exakt beräkna din sidstorlek i pixlar baserat på zoomfaktor och upplösning för optimal visning.
type: docs
weight: 90
url: /sv/net/aspose.words.rendering/pageinfo/getsizeinpixels/
---
## GetSizeInPixels(*float, float*) {#getsizeinpixels}

Beräknar sidstorleken i pixlar för en angiven zoomfaktor och upplösning.

```csharp
public Size GetSizeInPixels(float scale, float dpi)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| scale | Single | Zoomfaktorn (1,0 är 100 %). |
| dpi | Single | Upplösningen (horisontell och vertikal) som ska konverteras från punkter till pixlar (punkter per tum). |

### Returvärde

Sidans storlek i pixlar.

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

---

## GetSizeInPixels(*float, float, float*) {#getsizeinpixels_1}

Beräknar sidstorleken i pixlar för en angiven zoomfaktor och upplösning.

```csharp
public Size GetSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| scale | Single | Zoomfaktorn (1,0 är 100 %). |
| horizontalDpi | Single | Den horisontella upplösningen som ska konverteras från punkter till pixlar (punkter per tum). |
| verticalDpi | Single | Den vertikala upplösningen som ska konverteras från punkter till pixlar (punkter per tum). |

### Returvärde

Sidans storlek i pixlar.

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
