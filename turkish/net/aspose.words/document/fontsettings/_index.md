---
title: Document.FontSettings
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words for .NET
description: Document FontSettings mülk. Belge yazı tipi ayarlarını alır veya ayarlar C#'da.
type: docs
weight: 140
url: /tr/net/aspose.words/document/fontsettings/
---
## Document.FontSettings property

Belge yazı tipi ayarlarını alır veya ayarlar.

```csharp
public FontSettings FontSettings { get; set; }
```

## Notlar

Bu özellik, belge başına yazı tipi ayarlarının belirlenmesine olanak tanır. Eğer ayarlanmışsa`hükümsüz` , varsayılan statik yazı tipi ayarları [`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) kullanılacak.

Varsayılan değer:`hükümsüz`.

## Örnekler

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

// Belirleyen bir yazı tipi değiştirme tablosu yapılandırabiliriz
// Aspose.Words'ün mevcut olmayan yazı tiplerinin yerine hangi yazı tiplerini kullanacağı.
// "Amethysta" için iki ikame yazı tipi ayarlayın: "Arvo" ve "Courier New".
// İlk ikame kullanılamıyorsa Aspose.Words ikinci ikameyi kullanmayı dener ve bu şekilde devam eder.
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

 // "Amethysta" kullanılamıyor ve değiştirme kuralı, yerine kullanılacak ilk yazı tipinin "Arvo" olduğunu belirtir.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

 // "Arvo" da mevcut değil, ancak "Courier New" mevcut.
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Çıktı belgesi "Courier New" ile biçimlendirilmiş "Amethysta" yazı tipini kullanan metni görüntüleyecektir.
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
```

### Ayrıca bakınız

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
