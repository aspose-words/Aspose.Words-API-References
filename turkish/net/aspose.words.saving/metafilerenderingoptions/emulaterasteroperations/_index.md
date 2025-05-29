---
title: MetafileRenderingOptions.EmulateRasterOperations
linktitle: EmulateRasterOperations
articleTitle: EmulateRasterOperations
second_title: .NET için Aspose.Words
description: Raster işlem emülasyonunu kontrol etmek ve işleme yeteneklerinizi etkili bir şekilde geliştirmek için MetafileRenderingOptions EmulateRasterOperations özelliğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/
---
## MetafileRenderingOptions.EmulateRasterOperations property

Raster işlemlerinin öykünülüp öykünülmeyeceğini belirleyen bir değer alır veya ayarlar.

```csharp
public bool EmulateRasterOperations { get; set; }
```

## Notlar

Belirli raster işlemleri meta dosyalarında kullanılabilir. Bunlar doğrudan vektör grafiklerine işlenemez. Raster işlemlerini taklit etmek, ortaya çıkan vektör grafiklerinin kısmi rasterleştirilmesini gerektirir ve bu da meta dosyası işleme performansını etkileyebilir.

Bu değer olarak ayarlandığında`doğru`, Aspose.Words raster işlemlerini taklit eder. Ortaya çıkan çıktı maybe kısmen rasterleştirilir ve performans daha yavaş olabilir.

Bu değer olarak ayarlandığında`YANLIŞ`, Aspose.Words raster işlemlerini taklit etmez. Aspose.Words bir meta dosyasında raster işlemiyle karşılaştığında, meta dosyasını x000d_ işletim sistemini kullanarak bir bit eşlemine dönüştürmeye geri döner.

Bu seçenek yalnızca meta dosyası vektör grafik olarak işlendiğinde kullanılır.

Varsayılan değer:`doğru`.

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

* class [MetafileRenderingOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
