---
title: Description
second_title: Aspose.Words for .NET API Referansı
description: Uyarının açıklamasını döndürür.
type: docs
weight: 10
url: /tr/net/aspose.words/warninginfo/description/
---
## WarningInfo.Description property

Uyarının açıklamasını döndürür.

```csharp
public string Description { get; }
```

### Örnekler

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

* class [WarningInfo](../../warninginfo)
* ad alanı [Aspose.Words](../../warninginfo)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->