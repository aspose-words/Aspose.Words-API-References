---
title: DocumentBase.WarningCallback
linktitle: WarningCallback
articleTitle: WarningCallback
second_title: .NET için Aspose.Words
description: Belge işleme sırasında olası biçimlendirme sorunlarını tespit ederek veri bütünlüğünün sağlanması için hayati önem taşıyan DocumentBase WarningCallback özelliğini keşfedin.
type: docs
weight: 100
url: /tr/net/aspose.words/documentbase/warningcallback/
---
## DocumentBase.WarningCallback property

Çeşitli belge işleme prosedürleri sırasında, veri veya biçimlendirme sadakat kaybına neden olabilecek bir sorun algılandığında çağrılır.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## Notlar

Belgesi, varlığının herhangi bir aşamasında uyarılar üretebilir, bu nedenle uyarı kaybını önlemek için uyarı geri aramasını mümkün olduğunca erken as olarak ayarlamak önemlidir. Örneğin, şu özellikler gibi:[`PageCount`](../../document/pagecount/) aslında daha sonra işleme için kullanılan belge düzenini oluşturur ve düzen uyarıları, daha sonraki işleme çağrıları için yalnızca uyarı geri araması belirtilirse kaybolabilir.

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

* interface [IWarningCallback](../../iwarningcallback/)
* class [DocumentBase](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
