---
title: PageInfo.GetSizeInPixels
linktitle: GetSizeInPixels
articleTitle: GetSizeInPixels
second_title: Aspose.Words for .NET
description: PageInfo GetSizeInPixels yöntem. Belirtilen yakınlaştırma faktörü ve çözünürlük için sayfa boyutunu piksel cinsinden hesaplar C#'da.
type: docs
weight: 90
url: /tr/net/aspose.words.rendering/pageinfo/getsizeinpixels/
---
## GetSizeInPixels(*float, float*) {#getsizeinpixels}

Belirtilen yakınlaştırma faktörü ve çözünürlük için sayfa boyutunu piksel cinsinden hesaplar.

```csharp
public Size GetSizeInPixels(float scale, float dpi)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| scale | Single | Yakınlaştırma faktörü (1,0 %100'dür). |
| dpi | Single | Noktalardan piksellere (inç başına nokta sayısı) dönüştürülecek çözünürlük (yatay ve dikey). |

### Geri dönüş değeri

Sayfanın piksel cinsinden boyutu.

### Ayrıca bakınız

* class [PageInfo](../)
* ad alanı [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../../)

---

## GetSizeInPixels(*float, float, float*) {#getsizeinpixels_1}

Belirtilen yakınlaştırma faktörü ve çözünürlük için sayfa boyutunu piksel cinsinden hesaplar.

```csharp
public Size GetSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| scale | Single | Yakınlaştırma faktörü (1,0 %100'dür). |
| horizontalDpi | Single | Noktalardan piksellere (inç başına nokta) dönüştürülecek yatay çözünürlük. |
| verticalDpi | Single | Noktalardan piksellere (inç başına nokta) dönüştürülecek dikey çözünürlük. |

### Geri dönüş değeri

Sayfanın piksel cinsinden boyutu.

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
