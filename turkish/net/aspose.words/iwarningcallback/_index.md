---
title: IWarningCallback Interface
linktitle: IWarningCallback
articleTitle: IWarningCallback
second_title: .NET için Aspose.Words
description: Belge yükleme ve kaydetme sırasında doğruluk uyarılarını yakalama yöntemlerini özelleştirmek için Aspose.Words.IWarningCallback arayüzünü uygulayın. Belge bütünlüğünü geliştirin!
type: docs
weight: 3660
url: /tr/net/aspose.words/iwarningcallback/
---
## IWarningCallback interface

Belge yükleme veya kaydetme sırasında oluşabilecek sadakat kaybı uyarılarını yakalamak için kendi özel yönteminizi çağırmak istiyorsanız bu arayüzü uygulayın.

```csharp
public interface IWarningCallback
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Warning](../../aspose.words/iwarningcallback/warning/)(*[WarningInfo](../warninginfo/)*) | Aspose.Words, belge yükleme veya kaydetme sırasında biçimlendirme veya veri doğruluğu kaybına yol açabilecek bir sorunla karşılaştığında bu yöntemi çağırır. |

## Örnekler

Yazı tipi değiştirme uyarılarını izlemek için IWarningCallback arayüzünün nasıl kullanılacağını gösterir.

```csharp
public void SubstitutionWarning()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Times New Roman";
    builder.Writeln("Hello world!");

    FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
    doc.WarningCallback = callback;

    // Her belge için varsayılan yazı tipi kaynağı olacak olan geçerli yazı tipi kaynakları koleksiyonunu depola
    // bunun için farklı bir yazı tipi kaynağı belirtmiyoruz.
    FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

    // Test amaçlı olarak Aspose.Words'ü yalnızca var olmayan bir klasördeki fontları arayacak şekilde ayarlayacağız.
    FontSettings.DefaultInstance.SetFontsFolder(string.Empty, false);

    // Belgeyi işlerken "Times New Roman" yazı tipini bulabileceğimiz bir yer olmayacak.
    // Bu, geri aramamızın algılayacağı bir yazı tipi değiştirme uyarısına neden olacaktır.
    doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarning.pdf");

    FontSettings.DefaultInstance.SetFontsSources(originalFontSources);

    Assert.True(callback.FontSubstitutionWarnings[0].WarningType == WarningType.FontSubstitution);
    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Equals(
            "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font."));
}

private class FontSubstitutionWarningCollector : IWarningCallback
{
    /// <summary>
    /// Yükleme/kaydetme sırasında bir uyarı oluştuğunda her seferinde çağrılır.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontSubstitutionWarnings.Warning(info);
    }

    public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

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

Mevcut yazı tipi kaynaklarından eksik bir yazı tipi için en yakın eşleşmeyi bulma özelliğinin nasıl ayarlanacağını gösterir.

```csharp
public void EnableFontSubstitution()
{
    // Yazı tipi kaynaklarımızın hiçbirinde bulunmayan bir yazı tipiyle biçimlendirilmiş metin içeren bir belgeyi açın.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Yazı tipi değiştirme uyarılarını işlemek için bir geri çağırma atayın.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Varsayılan bir yazı tipi adı belirleyin ve yazı tipi değişimini etkinleştirin.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // Font değişiminden sonra orijinal font ölçütleri kullanılmalıdır.
    doc.LayoutOptions.KeepOriginalFontMetrics = true;

    // Eksik font içeren bir belgeyi kaydedersek font değiştirme uyarısı alırız.
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

    Assert.AreEqual(0, substitutionWarningHandler.FontWarnings.Count);
}

public class HandleDocumentSubstitutionWarnings : IWarningCallback
{
    /// <summary>
    /// Yükleme/kaydetme sırasında bir uyarı oluştuğunda her seferinde çağrılır.
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
