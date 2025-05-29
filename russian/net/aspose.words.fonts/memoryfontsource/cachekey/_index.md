---
title: MemoryFontSource.CacheKey
linktitle: CacheKey
articleTitle: CacheKey
second_title: Aspose.Words для .NET
description: Откройте для себя свойство MemoryFontSource CacheKey — откройте для себя эффективное кэширование с помощью уникального ключа для повышения производительности и оптимизации управления памятью.
type: docs
weight: 20
url: /ru/net/aspose.words.fonts/memoryfontsource/cachekey/
---
## MemoryFontSource.CacheKey property

Ключ этого источника в кэше.

```csharp
public string CacheKey { get; }
```

## Примечания

Этот ключ используется для идентификации элемента кэша при сохранении/загрузке кэша поиска шрифтов с помощью [`SaveSearchCache`](../../fontsettings/savesearchcache/) и[`SetFontsSources`](../../fontsettings/setfontssources/) методы.

## Примеры

Показывает, как ускорить процесс инициализации кэша шрифтов.

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
/// Загружать данные шрифта только при необходимости, а не сохранять их в памяти
/// на все время существования объекта "FontSettings".
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

### Смотрите также

* class [MemoryFontSource](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
