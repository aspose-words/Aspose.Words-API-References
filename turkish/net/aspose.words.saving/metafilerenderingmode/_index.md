---
title: Enum MetafileRenderingMode
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.MetafileRenderingMode Sıralama. Aspose.Wordsün WMF ve EMF meta dosyalarını nasıl oluşturacağını belirtir.
type: docs
weight: 5290
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
| VectorWithFallback | `0` | Aspose.Words bir meta dosyasını vektör grafikleri olarak işlemeye çalışır. Aspose.Words, meta dosyası kayıtlarından bazılarını vektör grafiklerine doğru şekilde işleyemezse, Aspose.Words bu meta dosyasını bir bitmap'e dönüştürür. |
| Vector | `1` | Aspose.Words bir meta dosyasını vektör grafikleri olarak işler. |
| Bitmap | `2` | Aspose.Words, bir meta dosyasını bir bitmap'e dönüştürmek için GDI+'yı çağırır ve ardından bitmap'i çıktı belgesine kaydeder. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


