---
title: MetafileRenderingMode
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Wordsün WMF ve EMF meta dosyalarını nasıl oluşturacağını belirtir.
type: docs
weight: 5010
url: /tr/net/aspose.words.saving/metafilerenderingmode/
---
## MetafileRenderingMode enumeration

Aspose.Words'ün WMF ve EMF meta dosyalarını nasıl oluşturacağını belirtir.

```csharp
public enum MetafileRenderingMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| VectorWithFallback | `0` | Aspose.Words, bir meta dosyasını vektör grafikleri olarak oluşturmaya çalışır. Aspose.Words, meta dosyası kayıtlarının bir kısmını vektör grafiklerine doğru şekilde işleyemezse, Aspose.Words bu meta dosyasını bir bitmap. olarak işler. |
| Vector | `1` | Aspose.Words, bir meta dosyasını vektör grafikleri olarak işler. |
| Bitmap | `2` | Aspose.Words, bir meta dosyasını bir bitmap'e dönüştürmek için GDI+'yı çağırır ve ardından bitmap'i çıktı belgesine kaydeder. |

### Örnekler

Gösteriler, bit eşlem oluşturmaya ve desteklenmeyen meta dosyası kayıtları hakkında uyarı türlerinin değiştirilmesine bir geri dönüş ekledi.

```csharp
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // Bitmap'e geri dönmek için "EmulateRasterOperations" özelliğini "false" olarak ayarlayın.
    // çıktı PDF'sinde tarama işlemleri gerektiren bir meta dosyayla karşılaşır.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // Her meta dosyasını vektör grafikleri kullanarak işlemeyi denemek için "RenderingMode" özelliğini "VectorWithFallback" olarak ayarlayın.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
    // bu yöntemin belgeyi .PDF'ye nasıl dönüştürdüğünü ve yapılandırmayı nasıl uyguladığını değiştirmek için
    // MetafileRenderingOptions nesnemizde kaydetme işlemine.
    PdfSaveOptions saveOptions = new PdfSaveOptions();
    saveOptions.MetafileRenderingOptions = metafileRenderingOptions;

    HandleDocumentWarnings callback = new HandleDocumentWarnings();
    doc.WarningCallback = callback;

    doc.Save(ArtifactsDir + "PdfSaveOptions.HandleBinaryRasterWarnings.pdf", saveOptions);

    Assert.AreEqual(1, callback.Warnings.Count);
    Assert.AreEqual("'R2_XORPEN' binary raster operation is partly supported.",
        callback.Warnings[0].Description);
}

/// <summary>
/// Bir belgeyi kaydettikten sonra oluşan biçimlendirme kaybıyla ilgili uyarıları yazdırır ve toplar.
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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->