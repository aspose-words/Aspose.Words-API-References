---
title: StreamFontSource.CacheKey
linktitle: CacheKey
articleTitle: CacheKey
second_title: Aspose.Words for .NET
description: 发现 StreamFontSource CacheKey 属性，通过高效缓存优化字体管理，以加快加载时间并增强性能。
type: docs
weight: 10
url: /zh/net/aspose.words.fonts/streamfontsource/cachekey/
---
## StreamFontSource.CacheKey property

缓存中此源的键。

```csharp
public string CacheKey { get; }
```

## 评论

此键用于在使用 保存/加载字体搜索缓存时识别缓存项[`SaveSearchCache`](../../fontsettings/savesearchcache/)和[`SetFontsSources`](../../fontsettings/setfontssources/)方法.

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

* class [StreamFontSource](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
