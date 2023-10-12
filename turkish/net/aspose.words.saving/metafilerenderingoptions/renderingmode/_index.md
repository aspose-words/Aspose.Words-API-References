---
title: MetafileRenderingOptions.RenderingMode
second_title: Aspose.Words for .NET API Referansı
description: MetafileRenderingOptions mülk. Meta dosyası görüntülerinin nasıl oluşturulması gerektiğini belirleyen bir değer alır veya ayarlar.
type: docs
weight: 60
url: /tr/net/aspose.words.saving/metafilerenderingoptions/renderingmode/
---
## MetafileRenderingOptions.RenderingMode property

Meta dosyası görüntülerinin nasıl oluşturulması gerektiğini belirleyen bir değer alır veya ayarlar.

```csharp
public MetafileRenderingMode RenderingMode { get; set; }
```

### Notlar

Varsayılan değer kaydetme biçimine bağlıdır. Görüntüler için öyleBitmap . Diğer formatlar içinVectorWithFallback.

### Örnekler

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

* enum [MetafileRenderingMode](../../metafilerenderingmode/)
* class [MetafileRenderingOptions](../)
* ad alanı [Aspose.Words.Saving](../../metafilerenderingoptions/)
* toplantı [Aspose.Words](../../../)


