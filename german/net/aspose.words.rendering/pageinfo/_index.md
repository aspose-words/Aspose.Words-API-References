---
title: PageInfo Class
linktitle: PageInfo
articleTitle: PageInfo
second_title: Aspose.Words für .NET
description: Aspose.Words.Rendering.PageInfo klas. Stellt Informationen zu einer bestimmten Dokumentseite dar in C#.
type: docs
weight: 4570
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
| [Colored](../../aspose.words.rendering/pageinfo/colored/) { get; } | Gibt zurück`WAHR` wenn die Seite farbige Inhalte enthält. |
| [HeightInPoints](../../aspose.words.rendering/pageinfo/heightinpoints/) { get; } | Ermittelt die Höhe der Seite in Punkten. |
| [Landscape](../../aspose.words.rendering/pageinfo/landscape/) { get; } | Gibt zurück`WAHR` wenn die im Dokument für diese Seite angegebene Seitenausrichtung Querformat ist. |
| [PaperSize](../../aspose.words.rendering/pageinfo/papersize/) { get; } | Ruft das Papierformat als Aufzählung ab. |
| [PaperTray](../../aspose.words.rendering/pageinfo/papertray/) { get; } | Ruft das Papierfach (Fach) für diese Seite ab, wie im Dokument angegeben. Der Wert ist Implementierungs-(Drucker-)spezifisch. |
| [SizeInPoints](../../aspose.words.rendering/pageinfo/sizeinpoints/) { get; } | Ermittelt die Seitengröße in Punkten. |
| [WidthInPoints](../../aspose.words.rendering/pageinfo/widthinpoints/) { get; } | Ermittelt die Breite der Seite in Punkten. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetDotNetPaperSize](../../aspose.words.rendering/pageinfo/getdotnetpapersize/)(*PaperSizeCollection*) | Ruft die abPaperSize Objekt, das zum Drucken der dadurch dargestellten Seite geeignet ist`PageInfo` . |
| [GetSizeInPixels](../../aspose.words.rendering/pageinfo/getsizeinpixels/#getsizeinpixels)(*float, float*) | Berechnet die Seitengröße in Pixel für einen angegebenen Zoomfaktor und eine bestimmte Auflösung. |
| [GetSizeInPixels](../../aspose.words.rendering/pageinfo/getsizeinpixels/#getsizeinpixels_1)(*float, float, float*) | Berechnet die Seitengröße in Pixel für einen angegebenen Zoomfaktor und eine bestimmte Auflösung. |
| [GetSpecifiedPrinterPaperSource](../../aspose.words.rendering/pageinfo/getspecifiedprinterpapersource/)(*PaperSourceCollection, PaperSource*) | Ruft die abPaperSource Objekt, das zum Drucken der dadurch dargestellten Seite geeignet ist`PageInfo` . |

## Bemerkungen

Die von diesem Objekt zurückgegebene Seitenbreite und -höhe stellen die „endgültige“ Größe der Seite dar, z. B. sind sie bereits in die richtige Ausrichtung gedreht.

## Beispiele

Zeigt, wie Seitengrößen- und Ausrichtungsinformationen für jede Seite in einem Word-Dokument gedruckt werden.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Der erste Abschnitt hat 2 Seiten. Wir werden jedem ein anderes Druckerpapierfach zuweisen,
// dessen Nummer mit einer Art Papierquelle übereinstimmt. Diese Quellen und ihre Arten können variieren
// abhängig vom installierten Druckertreiber.
PrinterSettings.PaperSourceCollection paperSources = new PrinterSettings().PaperSources;

doc.FirstSection.PageSetup.FirstPageTray = paperSources[0].RawKind;
doc.FirstSection.PageSetup.OtherPagesTray = paperSources[1].RawKind;

Console.WriteLine("Document \"{0}\" contains {1} pages.", doc.OriginalFileName, doc.PageCount);

float scale = 1.0f;
float dpi = 96;

for (int i = 0; i < doc.PageCount; i++)
{
    // Jede Seite hat ein PageInfo-Objekt, dessen Index die Nummer der jeweiligen Seite ist.
    PageInfo pageInfo = doc.GetPageInfo(i);

    // Ausrichtung und Abmessungen der Seite drucken.
    Console.WriteLine($"Page {i + 1}:");
    Console.WriteLine($"\tOrientation:\t{(pageInfo.Landscape ? "Landscape" : "Portrait")}");
    Console.WriteLine($"\tPaper size:\t\t{pageInfo.PaperSize} ({pageInfo.WidthInPoints:F0}x{pageInfo.HeightInPoints:F0}pt)");
    Console.WriteLine($"\tSize in points:\t{pageInfo.SizeInPoints}");
    Console.WriteLine($"\tSize in pixels:\t{pageInfo.GetSizeInPixels(1.0f, 96)} at {scale * 100}% scale, {dpi} dpi");

    // Drucken Sie die Informationen zum Quellfach.
    Console.WriteLine($"\tTray:\t{pageInfo.PaperTray}");
    PaperSource source = pageInfo.GetSpecifiedPrinterPaperSource(paperSources, paperSources[0]);
    Console.WriteLine($"\tSuitable print source:\t{source.SourceName}, kind: {source.Kind}");
}
```

### Siehe auch

* namensraum [Aspose.Words.Rendering](../../aspose.words.rendering/)
* Montage [Aspose.Words](../../)
