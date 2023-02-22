---
title: FontSettings.DefaultInstance
second_title: Aspose.Words for .NET API Referansı
description: FontSettings mülk. Statik varsayılan yazı tipi ayarları.
type: docs
weight: 20
url: /tr/net/aspose.words.fonts/fontsettings/defaultinstance/
---
## FontSettings.DefaultInstance property

Statik varsayılan yazı tipi ayarları.

```csharp
public static FontSettings DefaultInstance { get; }
```

### Notlar

Bu örnek, bir belgede varsayılan olarak kullanılır.[`FontSettings`](../../../aspose.words/document/fontsettings/) belirtildi.

### Örnekler

Varsayılan yazı tipi ayarları örneğinin nasıl yapılandırılacağını gösterir.

```csharp
// "Courier New" yazı tipini kullanmak için varsayılan yazı tipi ayarları örneğini yapılandırın
// Bilinmeyen bir yazı tipi kullanmaya çalıştığımızda yedek yedek olarak.
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.Enabled);

Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

// Bu belgede FontSettings yapılandırması yok. Belgeyi oluşturduğumuzda,
// varsayılan FontSettings örneği, eksik yazı tipini çözecektir.
// Aspose.Words, bilinmeyen yazı tipini kullanan metni oluşturmak için "Courier New" kullanacaktır.
Assert.Null(doc.FontSettings);

doc.Save(ArtifactsDir + "FontSettings.DefaultFontInstance.pdf");
```

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

### Ayrıca bakınız

* class [FontSettings](../)
* ad alanı [Aspose.Words.Fonts](../../fontsettings/)
* toplantı [Aspose.Words](../../../)


