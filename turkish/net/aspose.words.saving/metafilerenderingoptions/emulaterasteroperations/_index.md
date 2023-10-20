---
title: MetafileRenderingOptions.EmulateRasterOperations
linktitle: EmulateRasterOperations
articleTitle: EmulateRasterOperations
second_title: Aspose.Words for .NET
description: MetafileRenderingOptions EmulateRasterOperations mülk. Tarama işlemlerinin taklit edilip edilmeyeceğini belirleyen bir değer alır veya ayarlar C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/
---
## MetafileRenderingOptions.EmulateRasterOperations property

Tarama işlemlerinin taklit edilip edilmeyeceğini belirleyen bir değer alır veya ayarlar.

```csharp
public bool EmulateRasterOperations { get; set; }
```

## Notlar

Meta dosyalarda belirli tarama işlemleri kullanılabilir. Doğrudan vektör grafiklerine dönüştürülemezler. Raster işlemlerinin taklit edilmesi, elde edilen vektör grafiklerinin kısmi rasterleştirilmesini gerektirir; bu, the meta dosyası oluşturma performansını etkileyebilir.

Bu değer şu şekilde ayarlandığında`doğru`Aspose.Words tarama işlemlerini taklit eder. Ortaya çıkan çıktı belki kısmen rasterleştirildi ve performans daha yavaş olabilir.

Bu değer şu şekilde ayarlandığında`YANLIŞ`, Aspose.Words raster işlemlerini taklit etmez. Aspose.Words , bir meta dosyada bir raster işlemiyle karşılaştığında, the işletim sistemini kullanarak meta dosyasını bir bitmap'e dönüştürmeye geri döner.

Bu seçenek yalnızca meta dosyası vektör grafikleri olarak işlendiğinde kullanılır.

Varsayılan değer:`doğru`.

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

* class [MetafileRenderingOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
