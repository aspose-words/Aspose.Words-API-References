---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPage
linktitle: EmulateRenderingToSizeOnPage
articleTitle: EmulateRenderingToSizeOnPage
second_title: Aspose.Words for .NET
description: MetafileRenderingOptions EmulateRenderingToSizeOnPage mülk. Meta dosyası oluşturmanın meta dosya görüntüsünü sayfa boyutuna göre mi yoksa meta dosyanın varsayılan boyutunda görüntüsüne mi benzettiğini belirleyen bir değer alır veya ayarlar C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPage property

Meta dosyası oluşturmanın meta dosya görüntüsünü sayfa boyutuna göre mi yoksa meta dosyanın varsayılan boyutunda görüntüsüne mi benzettiğini belirleyen bir değer alır veya ayarlar.

```csharp
public bool EmulateRenderingToSizeOnPage { get; set; }
```

## Notlar

Meta dosyalar MS Word'de görüntülendiğinde, bazı grafikler gerçek meta dosya boyutuna göre piksel cinsinden ölçeklendirilebilir. Yani yakınlaştırma bile meta dosya görüntüsünü etkileyebilir.

Bu değer şu şekilde ayarlandığında`doğru` Aspose.Words sayfadaki meta dosya boyutuna göre oluşturmayı taklit eder. Piksel cinsinden boyut, sayfadaki meta dosya boyutundan ve belirtilen değerden hesaplanır.[`EmulateRenderingToSizeOnPageResolution`](../emulaterenderingtosizeonpageresolution/).

Bu değer şu şekilde ayarlandığında`YANLIŞ`Aspose.Words, meta dosyası oluşturmayı piksel cinsinden varsayılan boyutuna öykünür.

Bu seçenek yalnızca meta dosyası vektör grafikleri olarak işlendiğinde kullanılır.

Varsayılan değer:`doğru`.

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
