---
title: DefaultFontSubstitutionRule Class
linktitle: DefaultFontSubstitutionRule
articleTitle: DefaultFontSubstitutionRule
second_title: Aspose.Words for .NET
description: Aspose.Words.Fonts.DefaultFontSubstitutionRule sınıf. Varsayılan yazı tipi değiştirme kuralı C#'da.
type: docs
weight: 2840
url: /tr/net/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class

Varsayılan yazı tipi değiştirme kuralı.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Fontlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fonts/) dokümantasyon makalesi.

```csharp
public class DefaultFontSubstitutionRule : FontSubstitutionRule
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DefaultFontName](../../aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/) { get; set; } | Varsayılan yazı tipi adını alır veya ayarlar. |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Kuralın etkin olup olmadığını belirtir. |

## Notlar

Bu kural, orijinal yazı tipinin mevcut olmaması durumunda ikame için kullanılacak tek varsayılan yazı tipi adını tanımlar.

## Örnekler

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

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)
