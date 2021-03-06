---
title: FontSettings
second_title: Aspose.Words for .NET API Referansı
description: Belge yazı tipi ayarlarını alır veya ayarlar.
type: docs
weight: 140
url: /tr/net/aspose.words/document/fontsettings/
---
## Document.FontSettings property

Belge yazı tipi ayarlarını alır veya ayarlar.

```csharp
public FontSettings FontSettings { get; set; }
```

### Notlar

Bu özellik, belge başına yazı tipi ayarlarını belirlemeye izin verir. Null olarak ayarlanırsa, varsayılan statik yazı tipi settings [`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance) kullanılacak.

Varsayılan değer null'dur.

### Örnekler

Yazı tipi değiştirme kurallarının nasıl ayarlandığını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// Varsayılan yazı tipi kaynakları, belgenin kullandığı ilk yazı tipini içerir.
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// İkinci yazı tipi olan "Amethysta" kullanılamıyor.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Bir yazı tipi değiştirme tablosu yapılandırabiliriz.
// Aspose.Words'ün mevcut olmayan yazı tiplerinin yerine hangi yazı tiplerini kullanacağı.
// "Amethysta" için iki ikame yazı tipi ayarlayın: "Arvo" ve "Courier New".
// İlk ikame mevcut değilse, Aspose.Words ikinci ikameyi kullanmaya çalışır ve bu şekilde devam eder.
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

 // "Amethysta" kullanılamaz ve ikame kuralı, ikame olarak kullanılacak ilk yazı tipinin "Arvo" olduğunu belirtir.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

 // "Arvo" da mevcut değil, ancak "Courier New" mevcut.
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Çıktı belgesi, "Courier New" ile biçimlendirilmiş "Amethysta" yazı tipini kullanan metni görüntüleyecektir.
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
```

### Ayrıca bakınız

* class [FontSettings](../../../aspose.words.fonts/fontsettings)
* class [Document](../../document)
* ad alanı [Aspose.Words](../../document)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
