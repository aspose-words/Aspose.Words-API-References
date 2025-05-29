---
title: DefaultFontSubstitutionRule Class
linktitle: DefaultFontSubstitutionRule
articleTitle: DefaultFontSubstitutionRule
second_title: .NET için Aspose.Words
description: Kusursuz font yönetimi ve gelişmiş belge biçimlendirmesi için Aspose.Words.Fonts.DefaultFontSubstitutionRule sınıfını keşfedin. İş akışınızı bugün optimize edin!
type: docs
weight: 3250
url: /tr/net/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class

Varsayılan yazı tipi değiştirme kuralı.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yazı Tipleriyle Çalışma](https://docs.aspose.com/words/net/working-with-fonts/) belgeleme makalesi.

```csharp
public class DefaultFontSubstitutionRule : FontSubstitutionRule
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DefaultFontName](../../aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/) { get; set; } | Varsayılan yazı tipi adını alır veya ayarlar. |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Kuralın etkin olup olmadığını belirtir. |

## Notlar

Bu kural, orijinal yazı tipi mevcut değilse ikame için kullanılacak tek varsayılan yazı tipi adını tanımlar.

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

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)
