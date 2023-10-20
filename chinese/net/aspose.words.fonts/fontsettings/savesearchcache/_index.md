---
title: FontSettings.SaveSearchCache
linktitle: SaveSearchCache
articleTitle: SaveSearchCache
second_title: 用于 .NET 的 Aspose.Words
description: FontSettings SaveSearchCache 方法. 将字体搜索缓存保存到流中 在 C#.
type: docs
weight: 70
url: /zh/net/aspose.words.fonts/fontsettings/savesearchcache/
---
## FontSettings.SaveSearchCache method

将字体搜索缓存保存到流中。

```csharp
public void SaveSearchCache(Stream outputStream)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| outputStream | Stream | 输出流。 |

## 评论

看[`SetFontsSources`](../setfontssources/)方法描述以获取更多信息。

## 例子

展示如何加快字体缓存初始化过程。

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
/// 仅在需要时加载字体数据而不是将其存储在内存中
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

* class [FontSettings](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
