---
title: PageInfo.Landscape
second_title: Aspose.Words for .NET API Referansı
description: PageInfo mülk. İadelerdoğru bu sayfa için belgede belirtilen sayfa yönü yatay ise.
type: docs
weight: 30
url: /tr/net/aspose.words.rendering/pageinfo/landscape/
---
## PageInfo.Landscape property

İadeler`doğru` bu sayfa için belgede belirtilen sayfa yönü yatay ise.

```csharp
public bool Landscape { get; }
```

### Örnekler

Bir Word belgesindeki her sayfa için sayfa boyutu ve yön bilgilerinin nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// İlk bölüm 2 sayfadan oluşuyor. Her birine farklı bir yazıcı kağıt tepsisi atayacağız,
// numarası bir tür kağıt kaynağıyla eşleşecek. Bu kaynaklar ve çeşitleri farklılık gösterecektir
// yüklü yazıcı sürücüsüne bağlı olarak.
PrinterSettings.PaperSourceCollection paperSources = new PrinterSettings().PaperSources;

doc.FirstSection.PageSetup.FirstPageTray = paperSources[0].RawKind;
doc.FirstSection.PageSetup.OtherPagesTray = paperSources[1].RawKind;

Console.WriteLine("Document \"{0}\" contains {1} pages.", doc.OriginalFileName, doc.PageCount);

float scale = 1.0f;
float dpi = 96;

for (int i = 0; i < doc.PageCount; i++)
{
    // Her sayfanın, dizini ilgili sayfanın numarası olan bir PageInfo nesnesi vardır.
    PageInfo pageInfo = doc.GetPageInfo(i);

    // Sayfanın yönünü ve boyutlarını yazdırın.
    Console.WriteLine($"Page {i + 1}:");
    Console.WriteLine($"\tOrientation:\t{(pageInfo.Landscape ? "Landscape" : "Portrait")}");
    Console.WriteLine($"\tPaper size:\t\t{pageInfo.PaperSize} ({pageInfo.WidthInPoints:F0}x{pageInfo.HeightInPoints:F0}pt)");
    Console.WriteLine($"\tSize in points:\t{pageInfo.SizeInPoints}");
    Console.WriteLine($"\tSize in pixels:\t{pageInfo.GetSizeInPixels(1.0f, 96)} at {scale * 100}% scale, {dpi} dpi");

    // Kaynak tepsi bilgilerini yazdırın.
    Console.WriteLine($"\tTray:\t{pageInfo.PaperTray}");
    PaperSource source = pageInfo.GetSpecifiedPrinterPaperSource(paperSources, paperSources[0]);
    Console.WriteLine($"\tSuitable print source:\t{source.SourceName}, kind: {source.Kind}");
}
```

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
* ad alanı [Aspose.Words.Rendering](../../pageinfo/)
* toplantı [Aspose.Words](../../../)


