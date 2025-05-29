---
title: PageInfo.Landscape
linktitle: Landscape
articleTitle: Landscape
second_title: Aspose.Words per .NET
description: Scopri se l'orientamento della pagina del tuo documento è orizzontale con PageInfo. Garantisci un layout ottimale per presentazioni e stampe di grande impatto.
type: docs
weight: 30
url: /it/net/aspose.words.rendering/pageinfo/landscape/
---
## PageInfo.Landscape property

Restituisce`VERO` se l'orientamento della pagina specificato nel documento per questa pagina è orizzontale.

```csharp
public bool Landscape { get; }
```

## Esempi

Mostra come stampare le informazioni relative alle dimensioni e all'orientamento della pagina per ogni pagina di un documento Word.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// La prima sezione è composta da 2 pagine. Assegneremo a ciascuna un vassoio carta diverso,
// il cui numero corrisponderà a un tipo di fonte cartacea. Queste fonti e i loro tipi varieranno
// a seconda del driver della stampante installato.
PrinterSettings.PaperSourceCollection paperSources = new PrinterSettings().PaperSources;

doc.FirstSection.PageSetup.FirstPageTray = paperSources[0].RawKind;
doc.FirstSection.PageSetup.OtherPagesTray = paperSources[1].RawKind;

Console.WriteLine("Document \"{0}\" contains {1} pages.", doc.OriginalFileName, doc.PageCount);

float scale = 1.0f;
float dpi = 96;

for (int i = 0; i < doc.PageCount; i++)
{
    // Ogni pagina ha un oggetto PageInfo, il cui indice è il numero della rispettiva pagina.
    PageInfo pageInfo = doc.GetPageInfo(i);

    // Stampa l'orientamento e le dimensioni della pagina.
    Console.WriteLine($"Page {i + 1}:");
    Console.WriteLine($"\tOrientation:\t{(pageInfo.Landscape ? "Landscape" : "Portrait")}");
    Console.WriteLine($"\tPaper size:\t\t{pageInfo.PaperSize} ({pageInfo.WidthInPoints:F0}x{pageInfo.HeightInPoints:F0}pt)");
    Console.WriteLine($"\tSize in points:\t{pageInfo.SizeInPoints}");
    Console.WriteLine($"\tSize in pixels:\t{pageInfo.GetSizeInPixels(1.0f, 96)} at {scale * 100}% scale, {dpi} dpi");

    // Stampa le informazioni sul vassoio di origine.
    Console.WriteLine($"\tTray:\t{pageInfo.PaperTray}");
    PaperSource source = pageInfo.GetSpecifiedPrinterPaperSource(paperSources, paperSources[0]);
    Console.WriteLine($"\tSuitable print source:\t{source.SourceName}, kind: {source.Kind}");
}
```

Mostra come personalizzare la stampa dei documenti Aspose.Words.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

    MyPrintDocument printDoc = new MyPrintDocument(doc);
    printDoc.PrinterSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;
    printDoc.PrinterSettings.FromPage = 1;
    printDoc.PrinterSettings.ToPage = 1;

    printDoc.Print();
}

/// <summary>
/// Seleziona un formato carta, un orientamento e un vassoio carta appropriati durante la stampa.
/// </summary>
public class MyPrintDocument : PrintDocument
{
    public MyPrintDocument(Document document)
    {
        mDocument = document;
    }

    /// <summary>
    /// Inizializza l'intervallo di pagine da stampare in base alla selezione dell'utente.
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
     /// Chiamato prima della stampa di ogni pagina.
    /// </summary>
    protected override void OnQueryPageSettings(QueryPageSettingsEventArgs e)
    {
        base.OnQueryPageSettings(e);

         // Un singolo documento di Microsoft Word può avere più sezioni che specificano pagine con dimensioni diverse,
         // orientamenti e vassoi carta. Il framework di stampa .NET richiama questo codice prima
        // ogni pagina viene stampata, il che ci dà la possibilità di specificare come stampare la pagina corrente.
        PageInfo pageInfo = mDocument.GetPageInfo(mCurrentPage - 1);
        e.PageSettings.PaperSize = pageInfo.GetDotNetPaperSize(PrinterSettings.PaperSizes);

        // Microsoft Word memorizza l'origine della carta (vassoio della stampante) per ogni sezione come valore specifico della stampante.
        // Per ottenere il valore corretto del vassoio, sarà necessario utilizzare la proprietà "RawKind", che la stampante dovrebbe restituire.
        e.PageSettings.PaperSource.RawKind = pageInfo.PaperTray;
        e.PageSettings.Landscape = pageInfo.Landscape;
    }

    /// <summary>
     /// Chiamato per ogni pagina per renderla pronta per la stampa.
    /// </summary>
    protected override void OnPrintPage(PrintPageEventArgs e)
    {
        base.OnPrintPage(e);

        // Il motore di rendering Aspose.Words crea una pagina disegnata dall'origine (x = 0, y = 0) del foglio.
        // La stampante avrà un margine rigido che stamperà ogni pagina. Dobbiamo compensare con quel margine rigido.
        float hardOffsetX, hardOffsetY;

        // Di seguito sono riportati due metodi per impostare un margine rigido.
        if (e.PageSettings != null && e.PageSettings.HardMarginX != 0 && e.PageSettings.HardMarginY != 0)
        {
            // 1 - Tramite la proprietà "PageSettings".
            hardOffsetX = e.PageSettings.HardMarginX;
            hardOffsetY = e.PageSettings.HardMarginY;
        }
        else
        {
            // 2 - Utilizzando i nostri valori, se la proprietà "PageSettings" non è disponibile.
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

### Guarda anche

* class [PageInfo](../)
* spazio dei nomi [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* assemblea [Aspose.Words](../../../)
