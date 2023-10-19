---
title: MetafileRenderingOptions.UseEmfEmbeddedToWmf
linktitle: UseEmfEmbeddedToWmf
articleTitle: UseEmfEmbeddedToWmf
second_title: Aspose.Words for .NET
description: MetafileRenderingOptions UseEmfEmbeddedToWmf mülk. Gömülü EMF meta dosyalarına sahip WMF meta dosyalarının nasıl işlenmesi gerektiğini belirleyen bir değer alır veya ayarlar C#'da.
type: docs
weight: 70
url: /tr/net/aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/
---
## MetafileRenderingOptions.UseEmfEmbeddedToWmf property

Gömülü EMF meta dosyalarına sahip WMF meta dosyalarının nasıl işlenmesi gerektiğini belirleyen bir değer alır veya ayarlar.

```csharp
public bool UseEmfEmbeddedToWmf { get; set; }
```

## Notlar

WMF meta dosyaları gömülü EMF verilerini içerebilir. MS Word çoğu durumda gömülü EMF verilerini kullanır. GDI+ her zaman WMF verilerini kullanır.

Bu değer şu şekilde ayarlandığında`doğru`Aspose.Words, oluşturma sırasında gömülü EMF verilerini kullanır.

Bu değer şu şekilde ayarlandığında`YANLIŞ`Aspose.Words, oluşturma sırasında WMF verilerini kullanır.

Bu seçenek yalnızca meta dosyası vektör grafikleri olarak işlendiğinde kullanılır. Meta dosyası bitmap'e dönüştürüldüğünde, WMF verileri her zaman kullanılır.

Varsayılan değer:`doğru`.

## Örnekler

PDF'ye kaydederken Gelişmiş Windows Meta Dosyası ile ilgili işleme seçeneklerinin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// "EmfPlusDualRenderingMode" özelliğini "EmfPlusDualRenderingMode.Emf" olarak ayarlayın
// EMF+ ikili meta dosyasının yalnızca EMF kısmını işlemek için.
// "EmfPlusDualRenderingMode" özelliğini "EmfPlusDualRenderingMode.EmfPlus" olarak ayarlayın
// EMF+ ikili meta dosyasının EMF+ kısmını işlemek için.
// "EmfPlusDualRenderingMode" özelliğini "EmfPlusDualRenderingMode.EmfPlusWithFallback" olarak ayarlayın
// EMF+ kayıtlarının tümü destekleniyorsa, EMF+ ikili meta dosyasının EMF+ kısmını işlemek için.
// Aksi takdirde Aspose.Words EMF kısmını oluşturacaktır.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// Gömülü EMF verilerini oluşturmak için "UseEmfEmbeddedToWmf" özelliğini "true" olarak ayarlayın
// vektör grafikleri olarak oluşturabileceğimiz meta dosyalar için.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### Ayrıca bakınız

* class [MetafileRenderingOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
