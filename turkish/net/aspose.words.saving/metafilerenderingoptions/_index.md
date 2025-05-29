---
title: MetafileRenderingOptions Class
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: .NET için Aspose.Words
description: Belgelerinizde gelişmiş meta dosyası işleme denetimi ve özelleştirmesi için Aspose.Words.Saving.MetafileRenderingOptions'ı keşfedin. İş akışınızı bugün optimize edin!
type: docs
weight: 6080
url: /tr/net/aspose.words.saving/metafilerenderingoptions/
---
## MetafileRenderingOptions class

Ek meta dosyası oluşturma seçeneklerinin belirtilmesine olanak tanır.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Windows Meta Dosyalarını İşleme](https://docs.aspose.com/words/net/handling-windows-metafiles/) belgeleme makalesi.

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
| [EmfPlusDualRenderingMode](../../aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/) { get; set; } | EMF+ Dual meta dosyalarının nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [EmulateRasterOperations](../../aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/) { get; set; } | Raster işlemlerinin öykünülüp öykünülmeyeceğini belirleyen bir değer alır veya ayarlar. |
| [EmulateRenderingToSizeOnPage](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/) { get; set; } | Meta dosyası oluşturma işleminin meta dosyasının page üzerindeki boyuta göre görüntülenmesini mi yoksa meta dosyasının varsayılan boyutunda görüntülenmesini mi taklit edeceğini belirleyen bir değer alır veya ayarlar. |
| [EmulateRenderingToSizeOnPageResolution](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/) { get; set; } | Sayfadaki boyuta meta dosya oluşturma emülasyonu için piksel/inç cinsinden çözünürlüğü alır veya ayarlar. |
| [RenderingMode](../../aspose.words.saving/metafilerenderingoptions/renderingmode/) { get; set; } | Meta dosyası görüntülerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [UseEmfEmbeddedToWmf](../../aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/) { get; set; } | Gömülü EMF meta dosyalarına sahip WMF meta dosyalarının nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [UseGdiRasterOperationsEmulation](../../aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/) { get; set; } | GDI+'ın raster işlemleri emülasyonu için kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar. |

## Örnekler

Desteklenmeyen meta dosyası kayıtları hakkında bitmap oluşturma ve uyarı türlerini değiştirmeye yönelik bir geri dönüş eklendi.

```csharp
public void HandleBinaryRasterWarnings()
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // Bitmap'e geri dönmek için "EmulateRasterOperations" özelliğini "false" olarak ayarlayın
    // Çıktı PDF'inde işlenmesi için raster işlemlerinin gerekeceği bir meta dosyasıyla karşılaşır.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // Her meta dosyasını vektör grafikleri kullanarak işlemeyi denemek için "RenderingMode" özelliğini "VectorWithFallback" olarak ayarlayın.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
    // bu yöntemin belgeyi .PDF'ye nasıl dönüştüreceğini ve yapılandırmayı nasıl uygulayacağını değiştirmek için
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
/// Bir belgeyi kaydederken oluşan biçimlendirme kaybıyla ilgili uyarıları yazdırır ve toplar.
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
