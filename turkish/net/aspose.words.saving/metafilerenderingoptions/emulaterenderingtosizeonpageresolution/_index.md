---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution
linktitle: EmulateRenderingToSizeOnPageResolution
articleTitle: EmulateRenderingToSizeOnPageResolution
second_title: Aspose.Words for .NET
description: MetafileRenderingOptions EmulateRenderingToSizeOnPageResolution mülk. Meta dosyası oluşturmanın sayfadaki boyuta emülasyonu için çözünürlüğü inç başına piksel cinsinden alır veya ayarlar C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution property

Meta dosyası oluşturmanın sayfadaki boyuta emülasyonu için çözünürlüğü inç başına piksel cinsinden alır veya ayarlar.

```csharp
public int EmulateRenderingToSizeOnPageResolution { get; set; }
```

## Notlar

Bu seçenek yalnızca şu durumlarda kullanılır:[`EmulateRenderingToSizeOnPage`](../emulaterenderingtosizeonpage/) ayarlandı`doğru`.

Varsayılan değer 96'dır. Bu, varsayılan ekran çözünürlüğüdür. Yani meta dosya oluşturma, MS Word'deki meta dosyasının görüntüsünü %100 yakınlaştırma faktörüyle taklit edecektir.

## Örnekler

Meta dosyasının sayfadaki boyutuna göre nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// "EmulateRenderingToSizeOnPage" özelliğini "true" olarak ayarlayın
// sayfadaki meta dosya boyutuna göre oluşturmayı taklit etmek için.
// "EmulateRenderingToSizeOnPage" özelliğini "false" olarak ayarlayın
// meta dosyası oluşturmayı piksel cinsinden varsayılan boyutuna benzetmek için.
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPage = renderToSize;
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution = 50;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
```

### Ayrıca bakınız

* class [MetafileRenderingOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
