---
title: MetafileRenderingMode Enum
linktitle: MetafileRenderingMode
articleTitle: MetafileRenderingMode
second_title: .NET için Aspose.Words
description: Aspose.Words.Saving.MetafileRenderingMode'un, optimum belge kalitesi ve performansı için WMF ve EMF meta dosyası oluşturmayı nasıl geliştirdiğini keşfedin.
type: docs
weight: 6070
url: /tr/net/aspose.words.saving/metafilerenderingmode/
---
## MetafileRenderingMode enumeration

Aspose.Words'ün WMF ve EMF meta dosyalarını nasıl işleyeceğini belirtir.

```csharp
public enum MetafileRenderingMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| VectorWithFallback | `0` | Aspose.Words bir meta dosyasını vektör grafikleri olarak işlemeye çalışır. Aspose.Words meta dosyası kayıtlarının bazılarını vektör grafiklerine doğru şekilde işleyemezse Aspose.Words bu meta dosyasını bir bit eşlemine işler. |
| Vector | `1` | Aspose.Words bir meta dosyasını vektör grafikleri olarak işler. |
| Bitmap | `2` | Aspose.Words, bir meta dosyasını bir bit eşlemine dönüştürmek için GDI+'ı çağırır ve ardından bit eşlemini çıktı belgesine kaydeder. |

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
