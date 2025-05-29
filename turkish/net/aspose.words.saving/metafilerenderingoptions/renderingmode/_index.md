---
title: MetafileRenderingOptions.RenderingMode
linktitle: RenderingMode
articleTitle: RenderingMode
second_title: .NET için Aspose.Words
description: Metafile görüntülerinin nasıl işleneceğini kontrol etmek, grafik kalitenizi ve performansınızı artırmak için MetafileRenderingOptions RenderingMode özelliğini keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words.saving/metafilerenderingoptions/renderingmode/
---
## MetafileRenderingOptions.RenderingMode property

Meta dosyası görüntülerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar.

```csharp
public MetafileRenderingMode RenderingMode { get; set; }
```

## Notlar

Varsayılan değer, kaydetme biçimine bağlıdır. Görüntüler içinBitmap . Diğer formatlar içinVectorWithFallback.

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

* enum [MetafileRenderingMode](../../metafilerenderingmode/)
* class [MetafileRenderingOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
