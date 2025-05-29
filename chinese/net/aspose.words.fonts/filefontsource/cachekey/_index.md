---
title: FileFontSource.CacheKey
linktitle: CacheKey
articleTitle: CacheKey
second_title: Aspose.Words for .NET
description: 发现 FileFontSource CacheKey 属性，这是高效字体管理和优化缓存以提高性能的关键。
type: docs
weight: 20
url: /zh/net/aspose.words.fonts/filefontsource/cachekey/
---
## FileFontSource.CacheKey property

缓存中此源的键。

```csharp
public string CacheKey { get; }
```

## 评论

此键用于在使用 保存/加载字体搜索缓存时识别缓存项[`SaveSearchCache`](../../fontsettings/savesearchcache/)and [`SetFontsSources`](../../fontsettings/setfontssources/)方法。

如果没有指定键，则[`FilePath`](../filepath/)将被用作密钥。

## 例子

展示如何加速字体缓存初始化过程。

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
/// 仅在需要时加载字体数据，而不是将其存储在内存中
/// 在“FontSettings”对象的整个生命周期内。
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

### 也可以看看

* class [FileFontSource](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
