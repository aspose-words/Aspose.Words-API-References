---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPage
linktitle: EmulateRenderingToSizeOnPage
articleTitle: EmulateRenderingToSizeOnPage
second_title: .NET için Aspose.Words
description: EmulateRenderingToSizeOnPage özelliğinin meta dosyası oluşturmayı nasıl geliştirdiğini ve optimum görsel sonuçlar için doğru görüntüleme boyutlarını nasıl sağladığını keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPage property

Meta dosyası oluşturma işleminin meta dosyasının page üzerindeki boyuta göre görüntülenmesini mi yoksa meta dosyasının varsayılan boyutunda görüntülenmesini mi taklit edeceğini belirleyen bir değer alır veya ayarlar.

```csharp
public bool EmulateRenderingToSizeOnPage { get; set; }
```

## Notlar

Meta dosyaları MS Word'de görüntülendiğinde, bazı grafikler gerçek meta dosyası boyutuna (piksel) göre ölçeklenebilir. Yani yakınlaştırma bile meta dosyası görüntüsünü etkileyebilir.

Bu değer olarak ayarlandığında`doğru` Aspose.Words, sayfadaki meta dosya boyutuna göre işlemeyi taklit eder. Piksel cinsinden boyut, sayfadaki meta dosya boyutundan ve belirtilen değerden hesaplanır.[`EmulateRenderingToSizeOnPageResolution`](../emulaterenderingtosizeonpageresolution/).

Bu değer olarak ayarlandığında`YANLIŞ`, Aspose.Words meta dosyası oluşturmayı varsayılan piksel boyutuna göre taklit eder.

Bu seçenek yalnızca meta dosyası vektör grafik olarak işlendiğinde kullanılır.

Varsayılan değer:`doğru`.

## Örnekler

Sayfadaki boyuta göre meta dosyasının nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// "EmulateRenderingToSizeOnPage" özelliğini "true" olarak ayarlayın
// Sayfadaki meta dosya boyutuna göre işlemeyi taklit etmek için.
// "EmulateRenderingToSizeOnPage" özelliğini "false" olarak ayarlayın
// meta dosyası oluşturmayı varsayılan piksel boyutuna benzetmek için.
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPage = renderToSize;
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution = 50;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
```

### Ayrıca bakınız

* class [MetafileRenderingOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
