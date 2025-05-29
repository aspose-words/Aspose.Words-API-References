---
title: FontSubstitutionSettings.DefaultFontSubstitution
linktitle: DefaultFontSubstitution
articleTitle: DefaultFontSubstitution
second_title: .NET için Aspose.Words
description: DefaultFontSubstitution özelliğinin kusursuz tipografi için font ayarlarını nasıl optimize ettiğini keşfedin. Etkili font değiştirme kurallarıyla tasarımınızı geliştirin.
type: docs
weight: 10
url: /tr/net/aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/
---
## FontSubstitutionSettings.DefaultFontSubstitution property

Varsayılan yazı tipi değiştirme kuralıyla ilgili ayarlar.

```csharp
public DefaultFontSubstitutionRule DefaultFontSubstitution { get; }
```

## Örnekler

Varsayılan yazı tipi değiştirme kuralının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// FontSettings içindeki varsayılan değiştirme kuralını al.
// Bu kural, eksik olan tüm yazı tiplerini "Times New Roman" ile değiştirecektir.
DefaultFontSubstitutionRule defaultFontSubstitutionRule =
    fontSettings.SubstitutionSettings.DefaultFontSubstitution;
Assert.True(defaultFontSubstitutionRule.Enabled);
Assert.AreEqual("Times New Roman", defaultFontSubstitutionRule.DefaultFontName);

// Varsayılan yazı tipi alternatifini "Courier New" olarak ayarlayın.
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// Bir belge oluşturucu kullanarak, ikamenin gerçekleştiğini görmediğimiz bir yazı tipinde biraz metin ekleyin,
// ve ardından sonucu PDF'e dönüştürün.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Missing Font";
builder.Writeln("Line written in a missing font, which will be substituted with Courier New.");

doc.Save(ArtifactsDir + "FontSettings.DefaultFontSubstitutionRule.pdf");
```

### Ayrıca bakınız

* class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule/)
* class [FontSubstitutionSettings](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
