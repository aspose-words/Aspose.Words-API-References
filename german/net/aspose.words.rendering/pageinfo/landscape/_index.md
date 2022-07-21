---
title: Landscape
second_title: Aspose.Words für .NET-API-Referenz
description: Gibt wahr zurück wenn die im Dokument für diese Seite angegebene Seitenausrichtung Querformat ist.
type: docs
weight: 20
url: /de/net/aspose.words.rendering/pageinfo/landscape/
---
## PageInfo.Landscape property

Gibt wahr zurück, wenn die im Dokument für diese Seite angegebene Seitenausrichtung Querformat ist.

```csharp
public bool Landscape { get; }
```

### Beispiele

Zeigt, wie Informationen zur Seitengröße und Ausrichtung für jede Seite in einem Word-Dokument gedruckt werden.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Der erste Abschnitt hat 2 Seiten. Wir werden jedem einen anderen Druckerpapierschacht zuweisen,
// dessen Nummer mit einer Art Papierquelle übereinstimmt. Diese Quellen und ihre Arten variieren
// je nach installiertem Druckertreiber.
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

    // Informationen zum Quellfach drucken.
    Console.WriteLine($"\tTray:\t{pageInfo.PaperTray}");
    PaperSource source = pageInfo.GetSpecifiedPrinterPaperSource(paperSources, paperSources[0]);
    Console.WriteLine($"\tSuitable print source:\t{source.SourceName}, kind: {source.Kind}");
}
```

Zeigt, wie das Drucken von Aspose.Words-Dokumenten angepasst wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

    MyPrintDocument printDoc = new MyPrintDocument(doc);
    printDoc.PrinterSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;
    printDoc.PrinterSettings.FromPage = 1;
    printDoc.PrinterSettings.ToPage = 1;

    printDoc.Print();
}

/// <summary>
/// Wählt beim Drucken eine geeignete Papiergröße, Ausrichtung und Papierkassette aus.
/// </summary>
public class MyPrintDocument : PrintDocument
{
    public MyPrintDocument(Document document)
    {
        mDocument = document;
    }

    /// <summary>
    /// Initialisiert den Bereich der zu druckenden Seiten gemäß der Benutzerauswahl.
    /// </summary>
    protected override void OnBeginPrint(PrintEventArgs e)
    {
        base.OnBeginPrint(e);

        switch (PrinterSettings.PrintRange)
        {
            case System.Drawing.Printing.PrintRange.AllPages:
                mCurrentPage = 1;
                mPageTo = mDocument.PageCount;
                break;
            case System.Drawing.Printing.PrintRange.SomePages:
                mCurrentPage = PrinterSettings.FromPage;
                mPageTo = PrinterSettings.ToPage;
                break;
            default:
                throw new InvalidOperationException("Unsupported print range.");
        }
    }

    /// <summary>
    /// Wird aufgerufen, bevor jede Seite gedruckt wird. 
    /// </summary>
    protected override void OnQueryPageSettings(QueryPageSettingsEventArgs e)
    {
        base.OnQueryPageSettings(e);

        // Ein einzelnes Microsoft Word-Dokument kann mehrere Abschnitte haben, die Seiten mit unterschiedlichen Größen angeben, 
        // Ausrichtungen und Papierfächer. Das .NET-Druckframework ruft diesen Code zuvor auf 
        // Jede Seite wird gedruckt, was uns die Möglichkeit gibt, anzugeben, wie die aktuelle Seite gedruckt werden soll.
        PageInfo pageInfo = mDocument.GetPageInfo(mCurrentPage - 1);
        e.PageSettings.PaperSize = pageInfo.GetDotNetPaperSize(PrinterSettings.PaperSizes);

        // Microsoft Word speichert die Papierquelle (Druckfach) für jeden Abschnitt als druckerspezifischen Wert.
        // Um den korrekten Fachwert zu erhalten, müssen Sie die "RawKind"-Eigenschaft verwenden, die Ihr Drucker zurückgeben sollte.
        e.PageSettings.PaperSource.RawKind = pageInfo.PaperTray;
        e.PageSettings.Landscape = pageInfo.Landscape;
    }

    /// <summary>
    /// Wird für jede Seite aufgerufen, um sie zum Drucken zu rendern. 
    /// </summary>
    protected override void OnPrintPage(PrintPageEventArgs e)
    {
        base.OnPrintPage(e);

        // Aspose.Words-Rendering-Engine erstellt eine Seite, die vom Ursprung (x = 0, y = 0) des Papiers gezeichnet wird.
        // Es wird einen harten Rand im Drucker geben, der jede Seite rendert. Wir müssen diese harte Marge ausgleichen.
        float hardOffsetX, hardOffsetY;

        // Im Folgenden finden Sie zwei Möglichkeiten, einen harten Rand festzulegen.
        if (e.PageSettings != null && e.PageSettings.HardMarginX != 0 && e.PageSettings.HardMarginY != 0)
        {
            // 1 - Über die Eigenschaft "PageSettings".
            hardOffsetX = e.PageSettings.HardMarginX;
            hardOffsetY = e.PageSettings.HardMarginY;
        }
        else
        {
            // 2 - Verwenden unserer eigenen Werte, wenn die Eigenschaft "PageSettings" nicht verfügbar ist.
            hardOffsetX = 20;
            hardOffsetY = 20;
        }

        mDocument.RenderToScale(mCurrentPage, e.Graphics, -hardOffsetX, -hardOffsetY, 1.0f);

        mCurrentPage++;
        e.HasMorePages = mCurrentPage <= mPageTo;
    }

    private readonly Document mDocument;
    private int mCurrentPage;
    private int mPageTo;
}
```

### Siehe auch

* class [PageInfo](../../pageinfo)
* namensraum [Aspose.Words.Rendering](../../pageinfo)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
