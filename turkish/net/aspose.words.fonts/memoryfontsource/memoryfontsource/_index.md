---
title: MemoryFontSource
linktitle: MemoryFontSource
articleTitle: MemoryFontSource
second_title: .NET için Aspose.Words
description: Projelerinizde kusursuz font yönetimi için güçlü bir oluşturucu olan MemoryFontSource'u keşfedin. Tasarımınızı kolaylıkla ve verimli bir şekilde geliştirin!
type: docs
weight: 10
url: /tr/net/aspose.words.fonts/memoryfontsource/memoryfontsource/
---
## MemoryFontSource(*byte[]*) {#constructor}

İşlemci.

```csharp
public MemoryFontSource(byte[] fontData)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fontData | Byte[] | İkili yazı tipi verileri. |

## Örnekler

Bir font dosyasındaki verilerle bir bayt dizisinin font kaynağı olarak nasıl kullanılacağını gösterir.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### Ayrıca bakınız

* class [MemoryFontSource](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)

---

## MemoryFontSource(*byte[], int*) {#constructor_1}

İşlemci.

```csharp
public MemoryFontSource(byte[] fontData, int priority)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fontData | Byte[] | İkili yazı tipi verileri. |
| priority | Int32 | Yazı tipi kaynağı önceliği. Bkz.[`Priority`](../../fontsourcebase/priority/) Daha fazla bilgi için mülk açıklamasına bakın. |

## Örnekler

Bir font dosyasındaki verilerle bir bayt dizisinin font kaynağı olarak nasıl kullanılacağını gösterir.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### Ayrıca bakınız

* class [MemoryFontSource](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)

---

## MemoryFontSource(*byte[], int, string*) {#constructor_2}

İşlemci.

```csharp
public MemoryFontSource(byte[] fontData, int priority, string cacheKey)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fontData | Byte[] | İkili yazı tipi verileri. |
| priority | Int32 | Yazı tipi kaynağı önceliği. Bkz.[`Priority`](../../fontsourcebase/priority/) Daha fazla bilgi için mülk açıklamasına bakın. |
| cacheKey | String | Bu kaynağın anahtarı önbellekte. Bkz.[`CacheKey`](../cachekey/) Daha fazla bilgi için mülk açıklamasına bakın. |

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
/// Font verilerini hafızada saklamak yerine yalnızca gerektiğinde yükleyin
/// "FontSettings" nesnesinin tüm yaşam süresi boyunca.
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

* class [MemoryFontSource](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
