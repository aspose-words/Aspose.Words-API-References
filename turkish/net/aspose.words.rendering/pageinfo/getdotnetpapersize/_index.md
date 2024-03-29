---
title: PageInfo.GetDotNetPaperSize
linktitle: GetDotNetPaperSize
articleTitle: GetDotNetPaperSize
second_title: Aspose.Words for .NET
description: PageInfo GetDotNetPaperSize yöntem. AlırPaperSize yazdırmaya uygun nesne bununla temsil edilen sayfaPageInfo  C#'da.
type: docs
weight: 80
url: /tr/net/aspose.words.rendering/pageinfo/getdotnetpapersize/
---
## PageInfo.GetDotNetPaperSize method

AlırPaperSize yazdırmaya uygun nesne bununla temsil edilen sayfa[`PageInfo`](../) .

```csharp
public PaperSize GetDotNetPaperSize(PaperSizeCollection paperSizes)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| paperSizes | PaperSizeCollection | Mevcut kağıt boyutları. |

### Geri dönüş değeri

Kağıt boyutunu belirtmek için .NET yazdırma çerçevesinde kullanabileceğiniz bir nesne.

## Örnekler

Aspose.Words belgelerinin yazdırılmasının nasıl özelleştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

    MyPrintDocument printDoc = new MyPrintDocument(doc);
    printDoc.PrinterSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;
    printDoc.PrinterSettings.FromPage = 1;
    printDoc.PrinterSettings.ToPage = 1;

    printDoc.Print();
}

/// <summary>
/// Yazdırma sırasında uygun kağıt boyutunu, yönünü ve kağıt tepsisini seçer.
/// </summary>
public class MyPrintDocument : PrintDocument
{
    public MyPrintDocument(Document document)
    {
        mDocument = document;
    }

    /// <summary>
    /// Kullanıcı seçimine göre yazdırılacak sayfa aralığını başlatır.
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
     /// Her sayfa yazdırılmadan önce çağrılır.
    /// </summary>
    protected override void OnQueryPageSettings(QueryPageSettingsEventArgs e)
    {
        base.OnQueryPageSettings(e);

         // Tek bir Microsoft Word belgesi, farklı boyutlardaki sayfaları belirten birden fazla bölüme sahip olabilir,
         // yönler ve kağıt tepsileri. .NET yazdırma çerçevesi bu kodu daha önce çağırır.
        // her sayfa yazdırılır, bu da bize mevcut sayfanın nasıl yazdırılacağını belirleme şansı verir.
        PageInfo pageInfo = mDocument.GetPageInfo(mCurrentPage - 1);
        e.PageSettings.PaperSize = pageInfo.GetDotNetPaperSize(PrinterSettings.PaperSizes);

        // Microsoft Word, her bölüm için kağıt kaynağını (yazıcı tepsisi) yazıcıya özgü bir değer olarak saklar.
        // Doğru tepsi değerini elde etmek için yazıcınızın döndürmesi gereken "RawKind" özelliğini kullanmanız gerekecektir.
        e.PageSettings.PaperSource.RawKind = pageInfo.PaperTray;
        e.PageSettings.Landscape = pageInfo.Landscape;
    }

    /// <summary>
     /// Her sayfanın yazdırılmak üzere işlenmesi için çağrılır.
    /// </summary>
    protected override void OnPrintPage(PrintPageEventArgs e)
    {
        base.OnPrintPage(e);

        // Aspose.Words render motoru, kağıdın orijininden (x = 0, y = 0) çizilmiş bir sayfa oluşturur.
        // Yazıcıda her sayfayı işleyecek sert bir kenar boşluğu olacaktır. Bu zor marjı dengelememiz gerekiyor.
        float hardOffsetX, hardOffsetY;

        // Aşağıda sert kenar boşluğu ayarlamanın iki yolu verilmiştir.
        if (e.PageSettings != null && e.PageSettings.HardMarginX != 0 && e.PageSettings.HardMarginY != 0)
        {
            // 1 - "PageSettings" özelliği aracılığıyla.
            hardOffsetX = e.PageSettings.HardMarginX;
            hardOffsetY = e.PageSettings.HardMarginY;
        }
        else
        {
            // 2 - "PageSettings" özelliği mevcut değilse kendi değerlerimizi kullanma.
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

### Ayrıca bakınız

* class [PageInfo](../)
* ad alanı [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../../)
