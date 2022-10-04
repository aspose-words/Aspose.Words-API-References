---
title: IWarningCallback
second_title: Aspose.Words for .NET API Referansı
description: Belge yükleme veya kaydetme sırasında oluşabilecek aslına uygunluk kaybı uyarılarını yakalamak için kendi özel yönteminizin çağrılmasını istiyorsanız bu arabirimi uygulayın.
type: docs
weight: 3010
url: /tr/net/aspose.words/iwarningcallback/
---
## IWarningCallback interface

Belge yükleme veya kaydetme sırasında oluşabilecek aslına uygunluk kaybı uyarılarını yakalamak için kendi özel yönteminizin çağrılmasını istiyorsanız bu arabirimi uygulayın.

```csharp
public interface IWarningCallback
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Warning](../../aspose.words/iwarningcallback/warning/)(WarningInfo) | Aspose.Words, belge yükleme veya kaydetme sırasında biçimlendirme veya veri doğruluğu kaybına neden olabilecek bazı sorunlarla karşılaştığında bu yöntemi çağırır. |

### Örnekler

Yazı tipi değiştirme uyarılarını izlemek için IWarningCallback arabiriminin nasıl kullanılacağını gösterir.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Times New Roman";
    builder.Writeln("Hello world!");

    FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
    doc.WarningCallback = callback;

    // Her belge için varsayılan yazı tipi kaynağı olacak mevcut yazı tipi kaynakları koleksiyonunu saklayın
    // farklı bir yazı tipi kaynağı belirtmediğimiz.
    FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

    // Test amacıyla, Aspose.Words'ü sadece mevcut olmayan bir klasördeki fontları arayacak şekilde ayarlayacağız.
    FontSettings.DefaultInstance.SetFontsFolder(string.Empty, false);

    // Belgeyi oluştururken "Times New Roman" yazı tipini bulacağınız bir yer olmayacak.
    // Bu, geri aramamızın algılayacağı bir yazı tipi değiştirme uyarısına neden olur.
    doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarning.pdf");

    FontSettings.DefaultInstance.SetFontsSources(originalFontSources);

    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Equals(
            "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font."));
}

private class FontSubstitutionWarningCollector : IWarningCallback
{
    /// <summary>
    /// Yükleme/kaydetme sırasında her uyarı oluştuğunda çağrılır.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontSubstitutionWarnings.Warning(info);
    }

    public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

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

Mevcut yazı tipi kaynaklarından eksik bir yazı tipi için en yakın eşleşmeyi bulma özelliğinin nasıl ayarlanacağını gösterir.

```csharp
[Test]
public void EnableFontSubstitution()
{
    // Yazı tipi kaynaklarımızın hiçbirinde bulunmayan bir yazı tipiyle biçimlendirilmiş metin içeren bir belge açın.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Yazı tipi değiştirme uyarılarını işlemek için bir geri arama atayın.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Varsayılan bir yazı tipi adı ayarlayın ve yazı tipi değiştirmeyi etkinleştirin.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // Yazı tipi eksik olan bir belgeyi kaydedersek yazı tipi değiştirme uyarısı alırız.
    doc.FontSettings = fontSettings;
    doc.Save(ArtifactsDir + "FontSettings.EnableFontSubstitution.pdf");

    using (IEnumerator<WarningInfo> warnings = substitutionWarningHandler.FontWarnings.GetEnumerator())
        while (warnings.MoveNext())
            Console.WriteLine(warnings.Current.Description);

    // Ayrıca koleksiyondaki uyarıları doğrulayabilir ve temizleyebiliriz.
    Assert.AreEqual(WarningSource.Layout, substitutionWarningHandler.FontWarnings[0].Source);
    Assert.AreEqual(
        "Font '28 Days Later' has not been found. Using 'Calibri' font instead. Reason: alternative name from document.",
        substitutionWarningHandler.FontWarnings[0].Description);

    substitutionWarningHandler.FontWarnings.Clear();

    Assert.That(substitutionWarningHandler.FontWarnings, Is.Empty);
}

public class HandleDocumentSubstitutionWarnings : IWarningCallback
{
    /// <summary>
    /// Yükleme/kaydetme sırasında her uyarı oluştuğunda çağrılır.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontWarnings.Warning(info);
    }

    public WarningInfoCollection FontWarnings = new WarningInfoCollection();
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
