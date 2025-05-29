---
title: PageInfo.WidthInPoints
linktitle: WidthInPoints
articleTitle: WidthInPoints
second_title: Aspose.Words für .NET
description: Entdecken Sie die PageInfo WidthInPoints-Eigenschaft, um einfach die Seitenbreite in Punkten abzurufen und so die Formatierung und Layoutpräzision Ihres Dokuments zu verbessern.
type: docs
weight: 70
url: /de/net/aspose.words.rendering/pageinfo/widthinpoints/
---
## PageInfo.WidthInPoints property

Ruft die Breite der Seite in Punkten ab.

```csharp
public float WidthInPoints { get; }
```

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

* class [PageInfo](../)
* namensraum [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Montage [Aspose.Words](../../../)
