---
title: PageInfo.Landscape
linktitle: Landscape
articleTitle: Landscape
second_title: Aspose.Words für .NET
description: Mit PageInfo können Sie feststellen, ob Ihr Dokument im Querformat ausgerichtet ist. So gewährleisten Sie optimales Layout für beeindruckende Präsentationen und Ausdrucke.
type: docs
weight: 30
url: /de/net/aspose.words.rendering/pageinfo/landscape/
---
## PageInfo.Landscape property

Rückgaben`WAHR` wenn die im Dokument für diese Seite angegebene Seitenausrichtung Querformat ist.

```csharp
public bool Landscape { get; }
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

Zeigt, wie der Druck von Aspose.Words-Dokumenten angepasst wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

    MyPrintDocument printDoc = new MyPrintDocument(doc);
    printDoc.PrinterSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;
    printDoc.PrinterSettings.FromPage = 1;
    printDoc.PrinterSettings.ToPage = 1;

    printDoc.Print();
}

/// <summary>
/// Wählt beim Drucken ein geeignetes Papierformat, eine geeignete Ausrichtung und ein geeignetes Papierfach aus.
/// </summary>
public class MyPrintDocument : PrintDocument
{
    public MyPrintDocument(Document document)
    {
        mDocument = document;
    }

    /// <summary>
    /// Initialisiert den zu druckenden Seitenbereich entsprechend der Benutzerauswahl.
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
        /// Wird vor dem Drucken jeder Seite aufgerufen.
    /// </summary>
    protected override void OnQueryPageSettings(QueryPageSettingsEventArgs e)
    {
        base.OnQueryPageSettings(e);

            // Ein einzelnes Microsoft Word-Dokument kann mehrere Abschnitte enthalten, die Seiten mit unterschiedlichen Größen angeben,
            // Ausrichtungen und Papierfächer. Das .NET-Druckframework ruft diesen Code auf, bevor
        // Jede Seite wird gedruckt, was uns die Möglichkeit gibt, anzugeben, wie die aktuelle Seite gedruckt werden soll.
        PageInfo pageInfo = mDocument.GetPageInfo(mCurrentPage - 1);
        e.PageSettings.PaperSize = pageInfo.GetDotNetPaperSize(PrinterSettings.PaperSizes);

        // Microsoft Word speichert die Papierquelle (Druckerfach) für jeden Abschnitt als druckerspezifischen Wert.
        // Um den richtigen Fachwert zu erhalten, müssen Sie die Eigenschaft „RawKind“ verwenden, die Ihr Drucker zurückgeben sollte.
        e.PageSettings.PaperSource.RawKind = pageInfo.PaperTray;
        e.PageSettings.Landscape = pageInfo.Landscape;
    }

    /// <summary>
        /// Wird für jede Seite aufgerufen, um sie für den Druck zu rendern.
    /// </summary>
    protected override void OnPrintPage(PrintPageEventArgs e)
    {
        base.OnPrintPage(e);

        // Die Rendering-Engine von Aspose.Words erstellt eine Seite, die vom Ursprung (x = 0, y = 0) des Papiers aus gezeichnet wird.
        // Der Drucker verfügt über einen festen Rand, der jede Seite rendert. Wir benötigen diesen Abstand.
        float hardOffsetX, hardOffsetY;

        // Unten sind zwei Möglichkeiten zum Festlegen eines festen Rands aufgeführt.
        if (e.PageSettings != null && e.PageSettings.HardMarginX != 0 && e.PageSettings.HardMarginY != 0)
        {
            // 1 – Über die Eigenschaft „PageSettings“.
            hardOffsetX = e.PageSettings.HardMarginX;
            hardOffsetY = e.PageSettings.HardMarginY;
        }
        else
        {
            // 2 – Verwenden unserer eigenen Werte, wenn die Eigenschaft „PageSettings“ nicht verfügbar ist.
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

* class [PageInfo](../)
* namensraum [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Montage [Aspose.Words](../../../)
