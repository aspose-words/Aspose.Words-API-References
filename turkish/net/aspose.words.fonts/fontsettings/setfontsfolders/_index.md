---
title: FontSettings.SetFontsFolders
linktitle: SetFontsFolders
articleTitle: SetFontsFolders
second_title: .NET için Aspose.Words
description: Aspose.Words'de SetFontsFolders yönteminin, TrueType yazı tipi konumlarını en iyi belge oluşturma ve yerleştirme için nasıl özelleştirileceğini keşfedin.
type: docs
weight: 90
url: /tr/net/aspose.words.fonts/fontsettings/setfontsfolders/
---
## FontSettings.SetFontsFolders method

Aspose.Words'ün belgeleri işlerken veya yazı tiplerini yerleştirirken TrueType yazı tiplerini arayacağı klasörleri ayarlar.

```csharp
public void SetFontsFolders(string[] fontsFolders, bool recursive)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fontsFolders | String[] | TrueType yazı tiplerini içeren klasör dizisi. |
| recursive | Boolean | Belirtilen klasörleri yazı tipleri için yinelemeli olarak taramak için doğru. |

## Notlar

Varsayılan olarak Aspose.Words sisteme yüklenen yazı tiplerini arar.

Bu özelliğin ayarlanması, daha önce yüklenen tüm yazı tiplerinin önbelleğini sıfırlar.

## Örnekler

Birden fazla font kaynak dizininin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Yazı tipi kaynaklarımız bu belgede metin için kullandığımız yazı tipini içermiyor.
// Bu dokümanı oluştururken bu yazı tipi ayarlarını kullanırsak,
// Aspose.Words, Aspose.Words'ün bulamadığı bir yazı tipine sahip metne yedek bir yazı tipi uygulayacaktır.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Varsayılan yazı tipi kaynaklarında bu belgede kullandığımız iki yazı tipi eksik.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// İlk argüman olarak geçirdiğimiz her font dizininden bir font kaynağı oluşturmak için "SetFontsFolders" metodunu kullanın.
// Dizinlerdeki tüm yazı tipi dosyalarındaki yazı tiplerini dahil etmek için "yinelemeli" argüman olarak "false" değerini geçirin
// ilk argümanı geçiriyoruz ancak dizinlerin alt klasörlerinden hiçbir fontu dahil etmiyoruz.
// Geçirdiğimiz dizinlerdeki tüm yazı tipi dosyalarını dahil etmek için "tekrarlı" argüman olarak "true" değerini geçirin
// ilk argümanda ve alt dizinlerindeki tüm fontlarda.
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// "Junction" klasörünün kendisi herhangi bir font dosyası içermez, ancak bunu yapan alt klasörlere sahiptir.
if (recursive)
{
    Assert.AreEqual(6, newFontSources[1].GetAvailableFonts().Count);
    Assert.True(newFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));
}
else
{
    Assert.AreEqual(0, newFontSources[1].GetAvailableFonts().Count);
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolders.pdf");

// Orijinal yazı tipi kaynaklarını geri yükleyin.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Ayrıca bakınız

* class [FontSettings](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
