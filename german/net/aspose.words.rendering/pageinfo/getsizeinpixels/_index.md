---
title: PageInfo.GetSizeInPixels
linktitle: GetSizeInPixels
articleTitle: GetSizeInPixels
second_title: Aspose.Words für .NET
description: PageInfo GetSizeInPixels methode. Berechnet die Seitengröße in Pixel für einen angegebenen Zoomfaktor und eine bestimmte Auflösung in C#.
type: docs
weight: 90
url: /de/net/aspose.words.rendering/pageinfo/getsizeinpixels/
---
## GetSizeInPixels(*float, float*) {#getsizeinpixels}

Berechnet die Seitengröße in Pixel für einen angegebenen Zoomfaktor und eine bestimmte Auflösung.

```csharp
public Size GetSizeInPixels(float scale, float dpi)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| scale | Single | Der Zoomfaktor (1,0 ist 100 %). |
| dpi | Single | Die Auflösung (horizontal und vertikal), die von Punkten in Pixel (Punkte pro Zoll) umgewandelt werden soll. |

### Rückgabewert

Die Größe der Seite in Pixel.

### Siehe auch

* class [PageInfo](../)
* namensraum [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Montage [Aspose.Words](../../../)

---

## GetSizeInPixels(*float, float, float*) {#getsizeinpixels_1}

Berechnet die Seitengröße in Pixel für einen angegebenen Zoomfaktor und eine bestimmte Auflösung.

```csharp
public Size GetSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| scale | Single | Der Zoomfaktor (1,0 ist 100 %). |
| horizontalDpi | Single | Die horizontale Auflösung zur Konvertierung von Punkten in Pixel (Punkte pro Zoll). |
| verticalDpi | Single | Die vertikale Auflösung zur Konvertierung von Punkten in Pixel (Punkte pro Zoll). |

### Rückgabewert

Die Größe der Seite in Pixel.

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

* class [PageInfo](../)
* namensraum [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Montage [Aspose.Words](../../../)
