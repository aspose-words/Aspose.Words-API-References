---
title: PageInfo.GetDotNetPaperSize
linktitle: GetDotNetPaperSize
articleTitle: GetDotNetPaperSize
second_title: Aspose.Words för .NET
description: Upptäck GetDotNetPaperSize-metoden i PageInfo, utformad för att enkelt hämta det perfekta PaperSize-objektet för sömlös utskrift av sidor.
type: docs
weight: 80
url: /sv/net/aspose.words.rendering/pageinfo/getdotnetpapersize/
---
## PageInfo.GetDotNetPaperSize method

HämtarPaperSize objekt lämpligt för utskrift sidan som representeras av detta[`PageInfo`](../) .

```csharp
public PaperSize GetDotNetPaperSize(PaperSizeCollection paperSizes)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| paperSizes | PaperSizeCollection | Tillgängliga pappersstorlekar. |

### Returvärde

Ett objekt som du kan använda i .NET-utskriftsramverket för att ange pappersstorleken.

## Exempel

Visar hur man anpassar utskriften av Aspose.Words-dokument.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

    MyPrintDocument printDoc = new MyPrintDocument(doc);
    printDoc.PrinterSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;
    printDoc.PrinterSettings.FromPage = 1;
    printDoc.PrinterSettings.ToPage = 1;

    printDoc.Print();
}

/// <summary>
/// Väljer lämplig pappersstorlek, orientering och pappersfack vid utskrift.
/// </summary>
public class MyPrintDocument : PrintDocument
{
    public MyPrintDocument(Document document)
    {
        mDocument = document;
    }

    /// <summary>
    /// Initierar sidintervallet som ska skrivas ut enligt användarens val.
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
     /// Anropas innan varje sida skrivs ut.
    /// </summary>
    protected override void OnQueryPageSettings(QueryPageSettingsEventArgs e)
    {
        base.OnQueryPageSettings(e);

         // Ett enda Microsoft Word-dokument kan ha flera avsnitt som anger sidor med olika storlekar,
         // orienteringar och pappersfack. .NET-utskriftsramverket anropar denna kod innan
        // varje sida skrivs ut, vilket ger oss möjlighet att ange hur den aktuella sidan ska skrivas ut.
        PageInfo pageInfo = mDocument.GetPageInfo(mCurrentPage - 1);
        e.PageSettings.PaperSize = pageInfo.GetDotNetPaperSize(PrinterSettings.PaperSizes);

        // Microsoft Word lagrar papperskällan (skrivarfacket) för varje avsnitt som ett skrivarspecifikt värde.
        // För att få rätt värde för facket måste du använda egenskapen "RawKind", som din skrivare ska returnera.
        e.PageSettings.PaperSource.RawKind = pageInfo.PaperTray;
        e.PageSettings.Landscape = pageInfo.Landscape;
    }

    /// <summary>
     /// Anropade varje sida för att rendera den för utskrift.
    /// </summary>
    protected override void OnPrintPage(PrintPageEventArgs e)
    {
        base.OnPrintPage(e);

        // Aspose.Words renderingsmotor skapar en sida ritad från papprets origo (x = 0, y = 0).
        // Det kommer att finnas en hård marginal i skrivaren, som kommer att återge varje sida. Vi behöver förskjuta med den hårda marginalen.
        float hardOffsetX, hardOffsetY;

        // Nedan följer två sätt att ställa in en hård marginal.
        if (e.PageSettings != null && e.PageSettings.HardMarginX != 0 && e.PageSettings.HardMarginY != 0)
        {
            // 1 - Via egenskapen "Sidinställningar".
            hardOffsetX = e.PageSettings.HardMarginX;
            hardOffsetY = e.PageSettings.HardMarginY;
        }
        else
        {
            // 2 - Använder våra egna värden om egenskapen "PageSettings" inte är tillgänglig.
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

### Se även

* class [PageInfo](../)
* namnutrymme [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* hopsättning [Aspose.Words](../../../)
