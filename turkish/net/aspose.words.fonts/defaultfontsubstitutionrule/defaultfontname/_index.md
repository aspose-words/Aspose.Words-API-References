---
title: DefaultFontSubstitutionRule.DefaultFontName
linktitle: DefaultFontName
articleTitle: DefaultFontName
second_title: .NET için Aspose.Words
description: DefaultFontSubstitutionRule'u kolayca nasıl yöneteceğinizi ve gelişmiş tasarım esnekliği için varsayılan yazı tipi adınızı nasıl özelleştireceğinizi keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/
---
## DefaultFontSubstitutionRule.DefaultFontName property

Varsayılan yazı tipi adını alır veya ayarlar.

```csharp
public string DefaultFontName { get; set; }
```

## Notlar

Varsayılan değer 'Times New Roman'dır.

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

Varsayılan yazı tipinin nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// Belgenin kullandığı font kaynakları "Arial" fontunu içeriyor, ancak "Arvo" fontunu içermiyor.
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// "DefaultFontName" özelliğini "Courier New" olarak ayarlayın,
// belgeyi işlerken, başka bir yazı tipi mevcut olmadığında her durumda o yazı tipini uygula.
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Aspose.Words artık herhangi bir işleme çağrısı sırasında eksik yazı tipleri yerine varsayılan yazı tipini kullanacak.
doc.Save(ArtifactsDir + "FontSettings.DefaultFontName.pdf");
```

### Ayrıca bakınız

* class [DefaultFontSubstitutionRule](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
