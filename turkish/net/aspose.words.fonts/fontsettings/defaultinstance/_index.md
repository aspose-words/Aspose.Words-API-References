---
title: FontSettings.DefaultInstance
linktitle: DefaultInstance
articleTitle: DefaultInstance
second_title: .NET için Aspose.Words
description: Sorunsuz statik font yönetimi için FontSettings DefaultInstance özelliğini keşfedin. Özelleştirilebilir varsayılan ayarlarla tasarımınızı optimize edin!
type: docs
weight: 20
url: /tr/net/aspose.words.fonts/fontsettings/defaultinstance/
---
## FontSettings.DefaultInstance property

Statik varsayılan yazı tipi ayarları.

```csharp
public static FontSettings DefaultInstance { get; }
```

## Notlar

Bu örnek, bir belgede varsayılan olarak kullanılır, aksi takdirde[`FontSettings`](../../../aspose.words/document/fontsettings/) belirtildi.

## Örnekler

Varsayılan yazı tipi ayarları örneğinin nasıl yapılandırılacağını gösterir.

```csharp
// "Courier New" yazı tipini kullanmak için varsayılan yazı tipi ayarları örneğini yapılandırın
// bilinmeyen bir yazı tipini kullanmaya çalıştığımızda yedek bir yedek olarak.
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.Enabled);

Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

// Bu belgenin bir FontSettings yapılandırması yok. Belgeyi oluşturduğumuzda,
// Varsayılan FontSettings örneği eksik yazı tipini çözecektir.
// Aspose.Words, bilinmeyen yazı tipini kullanan metni oluşturmak için "Courier New" kullanacaktır.
Assert.Null(doc.FontSettings);

doc.Save(ArtifactsDir + "FontSettings.DefaultFontInstance.pdf");
```

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

### Ayrıca bakınız

* class [FontSettings](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
