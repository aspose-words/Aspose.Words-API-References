---
title: FontSettings.SetFontsSources
linktitle: SetFontsSources
articleTitle: SetFontsSources
second_title: Aspose.Words for .NET
description: FontSettings SetFontsSources yöntem. Aspose.Wordsün belgeleri oluştururken veya yazı tiplerini gömerken TrueType yazı tiplerini aradığı kaynakları ayarlar C#'da.
type: docs
weight: 100
url: /tr/net/aspose.words.fonts/fontsettings/setfontssources/
---
## SetFontsSources(*FontSourceBase[]*) {#setfontssources}

Aspose.Words'ün belgeleri oluştururken veya yazı tiplerini gömerken TrueType yazı tiplerini aradığı kaynakları ayarlar.

```csharp
public void SetFontsSources(FontSourceBase[] sources)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| sources | FontSourceBase[] | TrueType yazı tiplerini içeren bir dizi kaynak. |

## Notlar

Aspose.Words varsayılan olarak sistemde yüklü olan yazı tiplerini arar.

Bu özelliğin ayarlanması önceden yüklenen tüm yazı tiplerinin önbelleğini sıfırlar.

## Örnekler

Mevcut yazı tipi kaynaklarımıza nasıl yazı tipi kaynağı ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);

Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Varsayılan yazı tipi kaynağında, belgemizde kullandığımız yazı tiplerinden ikisi eksik.
// Bu belgeyi kaydettiğimizde Aspose.Words, erişilemeyen yazı tipleriyle biçimlendirilmiş tüm metinlere yedek yazı tiplerini uygulayacaktır.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Yazı tiplerini içeren bir klasörden yazı tipi kaynağı oluşturun.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Özel yazı tiplerimizin yanı sıra orijinal yazı tipi kaynaklarını da içeren yeni bir yazı tipi kaynakları dizisi uygulayın.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// Belgeyi PDF'ye dönüştürmeden önce Aspose.Words'ün gerekli tüm yazı tiplerine erişimi olduğunu doğrulayın.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// Orijinal yazı tipi kaynaklarını geri yükleyin.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Ayrıca bakınız

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)

---

## SetFontsSources(*FontSourceBase[], Stream*) {#setfontssources_1}

Aspose.Words'ün TrueType yazı tiplerini aradığı ve ayrıca önceden kaydedilmiş yazı tipi arama önbelleğini yüklediği kaynakları ayarlar.

```csharp
public void SetFontsSources(FontSourceBase[] sources, Stream cacheInputStream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| sources | FontSourceBase[] | TrueType yazı tiplerini içeren bir dizi kaynak. |
| cacheInputStream | Stream | Kaydedilmiş yazı tipi arama önbelleğiyle giriş akışı. |

## Notlar

Önceden kaydedilmiş yazı tipi arama önbelleğinin yüklenmesi, yazı tipi önbelleği başlatma sürecini hızlandıracaktır. is özellikle yazı tipi kaynaklarına erişimin karmaşık olduğu durumlarda faydalıdır (örn. yazı tipleri ağ üzerinden yüklendiğinde).

Yazı tipi arama önbelleği kaydedilirken ve yüklenirken, sağlanan kaynaklardaki yazı tipleri önbellek anahtarı aracılığıyla tanımlanır. Yazı tipleri için[`SystemFontSource`](../../systemfontsource/) Ve[`FolderFontSource`](../../folderfontsource/) önbellek anahtarı yazı tipi dosyasının yolu 'dir. İçin[`MemoryFontSource`](../../memoryfontsource/) Ve[`StreamFontSource`](../../streamfontsource/) önbellek anahtarı şurada tanımlı [`CacheKey`](../../memoryfontsource/cachekey/) Ve[`CacheKey`](../../streamfontsource/cachekey/) sırasıyla Properties . İçin[`FileFontSource`](../../filefontsource/) önbellek anahtarı ya[`CacheKey`](../../filefontsource/cachekey/) özelliği veya bir dosya yolu, eğer[`CacheKey`](../../filefontsource/cachekey/) dır-dir`hükümsüz`.

Önbellek yüklenirken, önbelleğin kaydedildiği andaki yazı tipi kaynaklarının aynısının sağlanması önemle tavsiye edilir. Yazı tipi kaynaklarındaki herhangi bir değişiklik (örn. yeni yazı tipleri eklemek, yazı tipi dosyalarını taşımak veya önbellek anahtarını değiştirmek), yazı tipinin hatalı olmasına yol açabilir Aspose.Words ile çözülüyor.

## Örnekler

Yazı tipi önbelleği başlatma işleminin nasıl hızlandırılacağını gösterir.

```csharp
public void LoadFontSearchCache()
{
    const string cacheKey1 = "Arvo";
    const string cacheKey2 = "Arvo-Bold";
    FontSettings parsedFonts = new FontSettings();
    FontSettings loadedCache = new FontSettings();

    parsedFonts.SetFontsSources(new FontSourceBase[]
    {
        new FileFontSource(FontsDir + "Arvo-Regular.ttf", 0, cacheKey1),
        new FileFontSource(FontsDir + "Arvo-Bold.ttf", 0, cacheKey2)
    });

    using (MemoryStream cacheStream = new MemoryStream())
    {
        parsedFonts.SaveSearchCache(cacheStream);
        loadedCache.SetFontsSources(new FontSourceBase[]
        {
            new SearchCacheStream(cacheKey1),                    
            new MemoryFontSource(File.ReadAllBytes(FontsDir + "Arvo-Bold.ttf"), 0, cacheKey2)
        }, cacheStream);
    }

    Assert.AreEqual(parsedFonts.GetFontsSources().Length, loadedCache.GetFontsSources().Length);
}

/// <summary>
/// Yazı tipi verilerini belleğe kaydetmek yerine yalnızca gerektiğinde yükleyin
/// "FontSettings" nesnesinin tüm ömrü boyunca.
/// </summary>
private class SearchCacheStream : StreamFontSource
{
    public SearchCacheStream(string cacheKey):base(0, cacheKey)
    {
    }

    public override Stream OpenFontDataStream()
    {
        return File.OpenRead(FontsDir + "Arvo-Regular.ttf");
    }
}
```

### Ayrıca bakınız

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
