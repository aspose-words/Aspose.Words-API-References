---
title: PageInfo.GetSpecifiedPrinterPaperSource
linktitle: GetSpecifiedPrinterPaperSource
articleTitle: GetSpecifiedPrinterPaperSource
second_title: Aspose.Words for .NET
description: PageInfo GetSpecifiedPrinterPaperSource yöntem. AlırPaperSource yazdırmaya uygun nesne bununla temsil edilen sayfaPageInfo  C#'da.
type: docs
weight: 100
url: /tr/net/aspose.words.rendering/pageinfo/getspecifiedprinterpapersource/
---
## PageInfo.GetSpecifiedPrinterPaperSource method

AlırPaperSource yazdırmaya uygun nesne bununla temsil edilen sayfa[`PageInfo`](../) .

```csharp
public PaperSource GetSpecifiedPrinterPaperSource(PaperSourceCollection paperSources, 
    PaperSource defaultPageSettingsPaperSource)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| paperSources | PaperSourceCollection | Mevcut kağıt kaynakları. |
| defaultPageSettingsPaperSource | PaperSource | Varsayılan yazıcı ayarlarında tanımlanan kağıt kaynağı. |

### Geri dönüş değeri

Kağıt kaynağını belirtmek için .NET yazdırma çerçevesinde kullanabileceğiniz bir nesne.

## Notlar

Bu yöntem .NET Framework 2.0 veya üstünü gerektirir.

## Örnekler

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

### Ayrıca bakınız

* class [PageInfo](../)
* ad alanı [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../../)
