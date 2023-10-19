---
title: MetafileRenderingOptions Class
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.MetafileRenderingOptions sınıf. Ek meta dosyası oluşturma seçeneklerini belirlemeye izin verir C#'da.
type: docs
weight: 5300
url: /tr/net/aspose.words.saving/metafilerenderingoptions/
---
## MetafileRenderingOptions class

Ek meta dosyası oluşturma seçeneklerini belirlemeye izin verir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Windows Meta Dosyalarını İşleme](https://docs.aspose.com/words/net/handling-windows-metafiles/) dokümantasyon makalesi.

```csharp
public class MetafileRenderingOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [MetafileRenderingOptions](metafilerenderingoptions/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [EmfPlusDualRenderingMode](../../aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/) { get; set; } | EMF+ Dual meta dosyalarının nasıl oluşturulması gerektiğini belirleyen bir değer alır veya ayarlar. |
| [EmulateRasterOperations](../../aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/) { get; set; } | Tarama işlemlerinin taklit edilip edilmeyeceğini belirleyen bir değer alır veya ayarlar. |
| [EmulateRenderingToSizeOnPage](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/) { get; set; } | Meta dosyası oluşturmanın meta dosya görüntüsünü sayfa boyutuna göre mi yoksa meta dosyanın varsayılan boyutunda görüntüsüne mi benzettiğini belirleyen bir değer alır veya ayarlar. |
| [EmulateRenderingToSizeOnPageResolution](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/) { get; set; } | Meta dosyası oluşturmanın sayfadaki boyuta emülasyonu için çözünürlüğü inç başına piksel cinsinden alır veya ayarlar. |
| [RenderingMode](../../aspose.words.saving/metafilerenderingoptions/renderingmode/) { get; set; } | Meta dosyası görüntülerinin nasıl oluşturulması gerektiğini belirleyen bir değer alır veya ayarlar. |
| [UseEmfEmbeddedToWmf](../../aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/) { get; set; } | Gömülü EMF meta dosyalarına sahip WMF meta dosyalarının nasıl işlenmesi gerektiğini belirleyen bir değer alır veya ayarlar. |
| [UseGdiRasterOperationsEmulation](../../aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/) { get; set; } | Tarama işlemleri emülasyonu için GDI+'nın kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |

## Örnekler

Gösteriler, bitmap oluşturmaya bir geri dönüş ekledi ve desteklenmeyen meta dosyası kayıtlarıyla ilgili uyarı türlerini değiştirdi.

```csharp
public void HandleBinaryRasterWarnings()
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // Bitmap'e geri dönmek için "EmulateRasterOperations" özelliğini "false" olarak ayarlayın
    // çıktı PDF'sinde görüntü oluşturmak için tarama işlemleri gerektiren bir meta dosyayla karşılaşır.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // Her meta dosyasını vektör grafikleri kullanarak oluşturmayı denemek için "RenderingMode" özelliğini "VectorWithFallback" olarak ayarlayın.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
    // bu yöntemin belgeyi .PDF'ye dönüştürme ve yapılandırmayı uygulama biçimini değiştirmek için
    // MetafileRenderingOptions nesnemizde kaydetme işlemine.
    PdfSaveOptions saveOptions = new PdfSaveOptions();
    saveOptions.MetafileRenderingOptions = metafileRenderingOptions;

    HandleDocumentWarnings callback = new HandleDocumentWarnings();
    doc.WarningCallback = callback;

    doc.Save(ArtifactsDir + "PdfSaveOptions.HandleBinaryRasterWarnings.pdf", saveOptions);

    Assert.AreEqual(1, callback.Warnings.Count);
    Assert.AreEqual("'R2_XORPEN' binary raster operation is not supported.",
        callback.Warnings[0].Description);
}

/// <summary>
/// Bir belge kaydedildiğinde oluşan biçimlendirme kaybıyla ilgili uyarıları yazdırır ve toplar.
/// </summary>
public class HandleDocumentWarnings : IWarningCallback
{
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.MinorFormattingLoss)
        {
            Console.WriteLine("Unsupported operation: " + info.Description);
            Warnings.Warning(info);
        }
    }

    public WarningInfoCollection Warnings = new WarningInfoCollection();
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
