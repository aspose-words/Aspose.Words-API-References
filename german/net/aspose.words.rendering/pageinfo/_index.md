---
title: PageInfo Class
linktitle: PageInfo
articleTitle: PageInfo
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Rendering.PageInfo, die wichtige Details zu jeder Dokumentseite bereitstellt und so Ihr Dokument-Rendering-Erlebnis verbessert.
type: docs
weight: 5300
url: /de/net/aspose.words.rendering/pageinfo/
---
## PageInfo class

Stellt Informationen zu einer bestimmten Dokumentseite dar.

Um mehr zu erfahren, besuchen Sie die[Rendern](https://docs.aspose.com/words/net/rendering/) Dokumentationsartikel.

```csharp
public class PageInfo
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Colored](../../aspose.words.rendering/pageinfo/colored/) { get; } | Rückgaben`WAHR` wenn die Seite farbigen Inhalt enthält. |
| [HeightInPoints](../../aspose.words.rendering/pageinfo/heightinpoints/) { get; } | Ruft die Höhe der Seite in Punkten ab. |
| [Landscape](../../aspose.words.rendering/pageinfo/landscape/) { get; } | Rückgaben`WAHR` wenn die im Dokument für diese Seite angegebene Seitenausrichtung Querformat ist. |
| [PaperSize](../../aspose.words.rendering/pageinfo/papersize/) { get; } | Ruft die Papiergröße als Aufzählung ab. |
| [PaperTray](../../aspose.words.rendering/pageinfo/papertray/) { get; } | Ruft das Papierfach (Fach) für diese Seite ab, wie im Dokument angegeben. Der Wert ist implementierungsspezifisch (druckerspezifisch). |
| [SizeInPoints](../../aspose.words.rendering/pageinfo/sizeinpoints/) { get; } | Ruft die Seitengröße in Punkten ab. |
| [WidthInPoints](../../aspose.words.rendering/pageinfo/widthinpoints/) { get; } | Ruft die Breite der Seite in Punkten ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetDotNetPaperSize](../../aspose.words.rendering/pageinfo/getdotnetpapersize/)(*PaperSizeCollection*) | Ruft diePaperSize Objekt geeignet zum Drucken die Seite, die durch dieses`PageInfo` . |
| [GetSizeInPixels](../../aspose.words.rendering/pageinfo/getsizeinpixels/#getsizeinpixels)(*float, float*) | Berechnet die Seitengröße in Pixeln für einen angegebenen Zoomfaktor und eine angegebene Auflösung. |
| [GetSizeInPixels](../../aspose.words.rendering/pageinfo/getsizeinpixels/#getsizeinpixels_1)(*float, float, float*) | Berechnet die Seitengröße in Pixeln für einen angegebenen Zoomfaktor und eine angegebene Auflösung. |
| [GetSpecifiedPrinterPaperSource](../../aspose.words.rendering/pageinfo/getspecifiedprinterpapersource/)(*PaperSourceCollection, PaperSource*) | Ruft diePaperSource Objekt geeignet zum Drucken die Seite, die durch dieses`PageInfo` . |

## Bemerkungen

Die von diesem Objekt zurückgegebene Seitenbreite und -höhe stellen die „endgültige“ Größe der Seite dar, d. h. sie sind bereits in die richtige Ausrichtung gedreht.

## Beispiele

Zeigt, wie Seitengrößen- und Ausrichtungsinformationen für jede Seite eines Word-Dokuments gedruckt werden.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Der erste Abschnitt besteht aus zwei Seiten. Wir weisen jeder Seite ein anderes Druckerpapierfach zu.
// deren Nummer einer Papierquelle entspricht. Diese Quellen und ihre Arten variieren
// abhängig vom installierten Druckertreiber.
PrinterSettings.PaperSourceCollection paperSources = new PrinterSettings().PaperSources;

doc.FirstSection.PageSetup.FirstPageTray = paperSources[0].RawKind;
doc.FirstSection.PageSetup.OtherPagesTray = paperSources[1].RawKind;

Console.WriteLine("Document \"{0}\" contains {1} pages.", doc.OriginalFileName, doc.PageCount);

float scale = 1.0f;
float dpi = 96;

for (int i = 0; i < doc.PageCount; i++)
{
    // Jede Seite hat ein PageInfo-Objekt, dessen Index die jeweilige Seitennummer ist.
    PageInfo pageInfo = doc.GetPageInfo(i);

    // Drucken Sie die Ausrichtung und Abmessungen der Seite.
    Console.WriteLine($"Page {i + 1}:");
    Console.WriteLine($"\tOrientation:\t{(pageInfo.Landscape ? "Landscape" : "Portrait")}");
    Console.WriteLine($"\tPaper size:\t\t{pageInfo.PaperSize} ({pageInfo.WidthInPoints:F0}x{pageInfo.HeightInPoints:F0}pt)");
    Console.WriteLine($"\tSize in points:\t{pageInfo.SizeInPoints}");
    Console.WriteLine($"\tSize in pixels:\t{pageInfo.GetSizeInPixels(1.0f, 96)} at {scale * 100}% scale, {dpi} dpi");

    // Druckt die Quellfachinformationen.
    Console.WriteLine($"\tTray:\t{pageInfo.PaperTray}");
    PaperSource source = pageInfo.GetSpecifiedPrinterPaperSource(paperSources, paperSources[0]);
    Console.WriteLine($"\tSuitable print source:\t{source.SourceName}, kind: {source.Kind}");
}
```

### Siehe auch

* namensraum [Aspose.Words.Rendering](../../aspose.words.rendering/)
* Montage [Aspose.Words](../../)
