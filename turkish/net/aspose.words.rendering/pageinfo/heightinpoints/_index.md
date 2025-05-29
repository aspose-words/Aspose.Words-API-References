---
title: PageInfo.HeightInPoints
linktitle: HeightInPoints
articleTitle: HeightInPoints
second_title: .NET için Aspose.Words
description: Sayfa yüksekliğine noktalar halinde kolayca erişmek için PageInfo'nun HeightInPoints özelliğini keşfedin. Belge düzeninizi hassas ölçümlerle geliştirin!
type: docs
weight: 20
url: /tr/net/aspose.words.rendering/pageinfo/heightinpoints/
---
## PageInfo.HeightInPoints property

Sayfanın yüksekliğini puan olarak alır.

```csharp
public float HeightInPoints { get; }
```

## Örnekler

Word belgesindeki her sayfa için sayfa boyutu ve yönlendirme bilgilerinin nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// İlk bölüm 2 sayfadan oluşuyor. Her birine farklı bir yazıcı kağıt tepsisi atayacağız.
// numarası bir tür kağıt kaynağıyla eşleşecek. Bu kaynaklar ve Türleri değişecektir
// yüklü yazıcı sürücüsüne bağlı olarak.
PrinterSettings.PaperSourceCollection paperSources = new PrinterSettings().PaperSources;

doc.FirstSection.PageSetup.FirstPageTray = paperSources[0].RawKind;
doc.FirstSection.PageSetup.OtherPagesTray = paperSources[1].RawKind;

Console.WriteLine("Document \"{0}\" contains {1} pages.", doc.OriginalFileName, doc.PageCount);

float scale = 1.0f;
float dpi = 96;

for (int i = 0; i < doc.PageCount; i++)
{
    // Her sayfanın bir PageInfo nesnesi vardır ve bu nesnenin indeksi ilgili sayfanın numarasıdır.
    PageInfo pageInfo = doc.GetPageInfo(i);

    // Sayfanın yönünü ve boyutlarını yazdır.
    Console.WriteLine($"Page {i + 1}:");
    Console.WriteLine($"\tOrientation:\t{(pageInfo.Landscape ? "Landscape" : "Portrait")}");
    Console.WriteLine($"\tPaper size:\t\t{pageInfo.PaperSize} ({pageInfo.WidthInPoints:F0}x{pageInfo.HeightInPoints:F0}pt)");
    Console.WriteLine($"\tSize in points:\t{pageInfo.SizeInPoints}");
    Console.WriteLine($"\tSize in pixels:\t{pageInfo.GetSizeInPixels(1.0f, 96)} at {scale * 100}% scale, {dpi} dpi");

    // Kaynak tepsi bilgilerini yazdır.
    Console.WriteLine($"\tTray:\t{pageInfo.PaperTray}");
    PaperSource source = pageInfo.GetSpecifiedPrinterPaperSource(paperSources, paperSources[0]);
    Console.WriteLine($"\tSuitable print source:\t{source.SourceName}, kind: {source.Kind}");
}
```

### Ayrıca bakınız

* class [PageInfo](../)
* ad alanı [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../../)
