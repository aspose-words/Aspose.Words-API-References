---
title: MemoryFontSource.MemoryFontSource
second_title: Aspose.Words for .NET API 参考
description: MemoryFontSource 构造函数. 向量.
type: docs
weight: 10
url: /zh/net/aspose.words.fonts/memoryfontsource/memoryfontsource/
---
## MemoryFontSource(byte[]) {#constructor}

向量.

```csharp
public MemoryFontSource(byte[] fontData)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontData | Byte[] | 二进制字体数据。 |

### 例子

演示如何使用字节数组和字体文件中的数据作为字体源。

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### 也可以看看

* class [MemoryFontSource](../)
* 命名空间 [Aspose.Words.Fonts](../../memoryfontsource/)
* 部件 [Aspose.Words](../../../)

---

## MemoryFontSource(byte[], int) {#constructor_1}

向量.

```csharp
public MemoryFontSource(byte[] fontData, int priority)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontData | Byte[] | 二进制字体数据。 |
| priority | Int32 | 字体来源优先。请参阅[`Priority`](../../fontsourcebase/priority/)属性描述以获取更多信息。 |

### 例子

演示如何使用字节数组和字体文件中的数据作为字体源。

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### 也可以看看

* class [MemoryFontSource](../)
* 命名空间 [Aspose.Words.Fonts](../../memoryfontsource/)
* 部件 [Aspose.Words](../../../)

---

## MemoryFontSource(byte[], int, string) {#constructor_2}

向量.

```csharp
public MemoryFontSource(byte[] fontData, int priority, string cacheKey)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontData | Byte[] | 二进制字体数据。 |
| priority | Int32 | 字体来源优先。请参阅[`Priority`](../../fontsourcebase/priority/)属性描述以获取更多信息。 |
| cacheKey | String | 缓存中该源的键。看[`CacheKey`](../cachekey/)属性描述以获取更多信息。 |

### 例子

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

* class [MemoryFontSource](../)
* 命名空间 [Aspose.Words.Fonts](../../memoryfontsource/)
* 部件 [Aspose.Words](../../../)


