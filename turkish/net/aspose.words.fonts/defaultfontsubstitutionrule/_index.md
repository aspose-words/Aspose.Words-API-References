---
title: Class DefaultFontSubstitutionRule
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fonts.DefaultFontSubstitutionRule sınıf. Varsayılan yazı tipi değiştirme kuralı.
type: docs
weight: 2660
url: /tr/net/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class

Varsayılan yazı tipi değiştirme kuralı.

```csharp
public class DefaultFontSubstitutionRule : FontSubstitutionRule
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DefaultFontName](../../aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/) { get; set; } | Varsayılan yazı tipi adını alır veya ayarlar. |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Kuralın etkin olup olmadığını belirtir. |

### Notlar

Bu kural, orijinal yazı tipi mevcut değilse, ikame için kullanılacak tek bir varsayılan yazı tipi adını tanımlar.

### Örnekler

Varsayılan yazı tipi değiştirme kuralının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// FontSettings içinde varsayılan ikame kuralını alın.
// Bu kural, tüm eksik yazı tiplerini "Times New Roman" ile değiştirecektir.
DefaultFontSubstitutionRule defaultFontSubstitutionRule =
    fontSettings.SubstitutionSettings.DefaultFontSubstitution;
Assert.True(defaultFontSubstitutionRule.Enabled);
Assert.AreEqual("Times New Roman", defaultFontSubstitutionRule.DefaultFontName);

// Varsayılan yazı tipi yerine "Courier New" olarak ayarlayın.
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// Bir belge oluşturucu kullanarak, ikamenin gerçekleştiğini görmemize gerek olmayan bir yazı tipine biraz metin ekleyin,
// ve ardından sonucu bir PDF'ye dönüştürün.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Missing Font";
builder.Writeln("Line written in a missing font, which will be substituted with Courier New.");

doc.Save(ArtifactsDir + "FontSettings.DefaultFontSubstitutionRule.pdf");
```

### Ayrıca bakınız

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)


