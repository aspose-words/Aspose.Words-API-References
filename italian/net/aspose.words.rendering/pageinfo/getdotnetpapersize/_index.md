---
title: PageInfo.GetDotNetPaperSize
linktitle: GetDotNetPaperSize
articleTitle: GetDotNetPaperSize
second_title: Aspose.Words per .NET
description: Scopri il metodo GetDotNetPaperSize in PageInfo, progettato per recuperare senza sforzo l'oggetto PaperSize ideale per una stampa di pagine senza interruzioni.
type: docs
weight: 80
url: /it/net/aspose.words.rendering/pageinfo/getdotnetpapersize/
---
## PageInfo.GetDotNetPaperSize method

Ottiene ilPaperSize oggetto adatto per stampare la pagina rappresentata da questo[`PageInfo`](../) .

```csharp
public PaperSize GetDotNetPaperSize(PaperSizeCollection paperSizes)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| paperSizes | PaperSizeCollection | Formati di carta disponibili. |

### Valore di ritorno

Oggetto che è possibile utilizzare nel framework di stampa .NET per specificare il formato della carta.

## Esempi

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
