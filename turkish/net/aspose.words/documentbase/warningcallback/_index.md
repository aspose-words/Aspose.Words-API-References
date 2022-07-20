---
title: WarningCallback
second_title: Aspose.Words for .NET API Referansı
description: Verilerde veya biçimlendirme aslına uygunluk kaybına neden olabilecek bir sorun algılandığında çeşitli belge işleme prosedürleri sırasında çağrılır.
type: docs
weight: 90
url: /tr/net/aspose.words/documentbase/warningcallback/
---
## DocumentBase.WarningCallback property

Verilerde veya biçimlendirme aslına uygunluk kaybına neden olabilecek bir sorun algılandığında çeşitli belge işleme prosedürleri sırasında çağrılır.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

### Notlar

Belge, varlığının herhangi bir aşamasında uyarılar üretebilir, bu nedenle uyarıların kaybolmasını önlemek için uyarı geri aramasını as olarak mümkün olduğunca erken ayarlamak önemlidir. Örneğin, gibi özellikler[`PageCount`](../../document/pagecount) aslında daha sonra işleme için kullanılan belge düzenini oluşturur ve yalnızca daha sonra işleme çağrıları için uyarı geri çağrısı belirtilirse düzen uyarıları kaybolabilir.

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

* interface [IWarningCallback](../../iwarningcallback)
* class [DocumentBase](../../documentbase)
* ad alanı [Aspose.Words](../../documentbase)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
