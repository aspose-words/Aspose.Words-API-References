---
title: Document.FontSettings
linktitle: FontSettings
articleTitle: FontSettings
second_title: .NET için Aspose.Words
description: Belge yazı tipi ayarlarını zahmetsizce nasıl özelleştireceğinizi keşfedin. Daha iyi okunabilirlik ve stil için özel yazı tipi seçenekleriyle belgelerinizi geliştirin.
type: docs
weight: 150
url: /tr/net/aspose.words/document/fontsettings/
---
## Document.FontSettings property

Belge yazı tipi ayarlarını alır veya ayarlar.

```csharp
public FontSettings FontSettings { get; set; }
```

## Notlar

Bu özellik, belge başına yazı tipi ayarlarını belirtmeye olanak tanır. Eğer ayarlanırsa`hükümsüz` , varsayılan statik yazı tipi ayarları [`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) kullanılacaktır.

Varsayılan değer:`hükümsüz`.

## Örnekler

Yazı tipi değiştirme kurallarının nasıl ayarlanacağını gösterir.

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

// İkinci font olan "Amethysta" mevcut değil.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Aşağıdakileri belirleyen bir yazı tipi değiştirme tablosu yapılandırabiliriz:
// Aspose.Words'ün kullanılamayan yazı tiplerinin yerine hangi yazı tiplerini kullanacağı.
// "Amethysta" için iki yedek yazı tipi ayarlayın: "Arvo" ve "Courier New".
// Eğer ilk ikame mevcut değilse, Aspose.Words ikinci ikameyi kullanmayı dener, vb.
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

 // "Amethysta" mevcut değil ve ikame kuralı, ikame olarak kullanılacak ilk fontun "Arvo" olduğunu belirtiyor.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

 // "Arvo" da mevcut değil, ancak "Courier New" mevcut.
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Çıktı belgesinde "Amethysta" yazı tipini kullanan metin "Courier New" ile biçimlendirilmiş olarak görüntülenecektir.
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
```

### Ayrıca bakınız

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
