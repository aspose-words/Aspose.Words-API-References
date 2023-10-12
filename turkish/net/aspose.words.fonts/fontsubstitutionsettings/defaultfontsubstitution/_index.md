---
title: FontSubstitutionSettings.DefaultFontSubstitution
second_title: Aspose.Words for .NET API Referansı
description: FontSubstitutionSettings mülk. Varsayılan yazı tipi değiştirme kuralıyla ilgili ayarlar.
type: docs
weight: 10
url: /tr/net/aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/
---
## FontSubstitutionSettings.DefaultFontSubstitution property

Varsayılan yazı tipi değiştirme kuralıyla ilgili ayarlar.

```csharp
public DefaultFontSubstitutionRule DefaultFontSubstitution { get; }
```

### Örnekler

Varsayılan yazı tipi değiştirme kuralının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// FontSettings'te varsayılan değiştirme kuralını alın.
// Bu kural, eksik olan tüm yazı tiplerini "Times New Roman" ile değiştirecektir.
DefaultFontSubstitutionRule defaultFontSubstitutionRule =
    fontSettings.SubstitutionSettings.DefaultFontSubstitution;
Assert.True(defaultFontSubstitutionRule.Enabled);
Assert.AreEqual("Times New Roman", defaultFontSubstitutionRule.DefaultFontName);

// Varsayılan yazı tipi alternatifini "Courier New" olarak ayarlayın.
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// Bir belge oluşturucu kullanarak, yazı tipine, değişikliğin gerçekleştiğini görmek zorunda kalmayacağımız bir miktar metin ekleyin,
// ve ardından sonucu bir PDF'ye dönüştürün.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Missing Font";
builder.Writeln("Line written in a missing font, which will be substituted with Courier New.");

doc.Save(ArtifactsDir + "FontSettings.DefaultFontSubstitutionRule.pdf");
```

### Ayrıca bakınız

* class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule/)
* class [FontSubstitutionSettings](../)
* ad alanı [Aspose.Words.Fonts](../../fontsubstitutionsettings/)
* toplantı [Aspose.Words](../../../)


