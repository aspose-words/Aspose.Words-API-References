---
title: PageInfo Class
linktitle: PageInfo
articleTitle: PageInfo
second_title: .NET için Aspose.Words
description: Her belge sayfası hakkında temel ayrıntıları sağlayan ve belge oluşturma deneyiminizi geliştiren Aspose.Words.Rendering.PageInfo sınıfını keşfedin.
type: docs
weight: 5300
url: /tr/net/aspose.words.rendering/pageinfo/
---
## PageInfo class

Belirli bir belge sayfasıyla ilgili bilgileri temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[İşleme](https://docs.aspose.com/words/net/rendering/) belgeleme makalesi.

```csharp
public class PageInfo
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Colored](../../aspose.words.rendering/pageinfo/colored/) { get; } | Geri Döndürür`doğru` eğer sayfa renkli içerik içeriyorsa. |
| [HeightInPoints](../../aspose.words.rendering/pageinfo/heightinpoints/) { get; } | Sayfanın yüksekliğini puan olarak alır. |
| [Landscape](../../aspose.words.rendering/pageinfo/landscape/) { get; } | Geri Döndürür`doğru` Bu sayfa için belgede belirtilen sayfa yönü yataysa. |
| [PaperSize](../../aspose.words.rendering/pageinfo/papersize/) { get; } | Kağıt boyutunu numaralandırma olarak alır. |
| [PaperTray](../../aspose.words.rendering/pageinfo/papertray/) { get; } | Belgede belirtilen şekilde bu sayfa için kağıt tepsisini (çöp kutusu) alır. Değer, uygulamaya (yazıcıya) özgüdür. |
| [SizeInPoints](../../aspose.words.rendering/pageinfo/sizeinpoints/) { get; } | Sayfa boyutunu puan olarak alır. |
| [WidthInPoints](../../aspose.words.rendering/pageinfo/widthinpoints/) { get; } | Sayfanın genişliğini noktalar halinde alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetDotNetPaperSize](../../aspose.words.rendering/pageinfo/getdotnetpapersize/)(*PaperSizeCollection*) | Şunu alır:PaperSize yazdırmaya uygun nesne bununla temsil edilen sayfa`PageInfo` . |
| [GetSizeInPixels](../../aspose.words.rendering/pageinfo/getsizeinpixels/#getsizeinpixels)(*float, float*) | Belirtilen yakınlaştırma faktörü ve çözünürlük için sayfa boyutunu piksel cinsinden hesaplar. |
| [GetSizeInPixels](../../aspose.words.rendering/pageinfo/getsizeinpixels/#getsizeinpixels_1)(*float, float, float*) | Belirtilen yakınlaştırma faktörü ve çözünürlük için sayfa boyutunu piksel cinsinden hesaplar. |
| [GetSpecifiedPrinterPaperSource](../../aspose.words.rendering/pageinfo/getspecifiedprinterpapersource/)(*PaperSourceCollection, PaperSource*) | Şunu alır:PaperSource yazdırmaya uygun nesne bununla temsil edilen sayfa`PageInfo` . |

## Notlar

Bu nesnenin döndürdüğü sayfa genişliği ve yüksekliği, sayfanın "son" boyutunu temsil eder, yani bunlar zaten doğru yönelime döndürülmüştür.

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

* ad alanı [Aspose.Words.Rendering](../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../)
