---
title: FontSettings.SetFontsSources
linktitle: SetFontsSources
articleTitle: SetFontsSources
second_title: 用于 .NET 的 Aspose.Words
description: FontSettings SetFontsSources 方法. 设置 Aspose.Words 在渲染文档或嵌入字体时查找 TrueType 字体的来源 在 C#.
type: docs
weight: 100
url: /zh/net/aspose.words.fonts/fontsettings/setfontssources/
---
## SetFontsSources(*FontSourceBase[]*) {#setfontssources}

设置 Aspose.Words 在渲染文档或嵌入字体时查找 TrueType 字体的来源。

```csharp
public void SetFontsSources(FontSourceBase[] sources)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sources | FontSourceBase[] | 包含 TrueType 字体的源数组。 |

## 评论

默认情况下，Aspose.Words 会查找安装到系统中的字体。

设置此属性会重置所有先前加载的字体的缓存。

## 例子

展示如何将字体源添加到我们现有的字体源。

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

// 默认字体源缺少我们在文档中使用的两种字体。
// 当我们保存这个文档时，Aspose.Words 会将后备字体应用到所有使用不可访问字体格式化的文本。
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// 从包含字体的文件夹创建字体源。
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// 应用一个新的字体源数组，其中包含原始字体源以及我们的自定义字体。
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// 在我们将文档呈现为 PDF 之前，验证 Aspose.Words 是否可以访问所有必需的字体。
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// 恢复原始字体源。
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### 也可以看看

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)

---

## SetFontsSources(*FontSourceBase[], Stream*) {#setfontssources_1}

设置 Aspose.Words 查找 TrueType 字体并额外加载之前保存的源 字体搜索缓存。

```csharp
public void SetFontsSources(FontSourceBase[] sources, Stream cacheInputStream)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sources | FontSourceBase[] | 包含 TrueType 字体的源数组。 |
| cacheInputStream | Stream | 具有已保存字体搜索缓存的输入流。 |

## 评论

加载以前保存的字体搜索缓存将加快字体缓存初始化过程。 is 在访问字体源很复杂时（例如通过网络加载字体时）特别有用。

保存和加载字体搜索缓存时，提供的源中的字体通过缓存键标识。 对于[`SystemFontSource`](../../systemfontsource/)和[`FolderFontSource`](../../folderfontsource/)缓存键是字体文件的 path 。为了[`MemoryFontSource`](../../memoryfontsource/)和[`StreamFontSource`](../../streamfontsource/)缓存键在 中定义[`CacheKey`](../../memoryfontsource/cachekey/)和[`CacheKey`](../../streamfontsource/cachekey/)properties 分别。为了[`FileFontSource`](../../filefontsource/)缓存键是[`CacheKey`](../../filefontsource/cachekey/) 属性或文件路径，如果[`CacheKey`](../../filefontsource/cachekey/)是**无效的**.

强烈建议在加载缓存时提供与保存缓存时相同的字体源。 字体源中的任何更改（例如添加新字体、移动字体文件或更改缓存键）都可能导致 字体不准确由 Aspose.Words 解决。

## 例子

显示如何加快字体缓存初始化过程。

```csharp
[Test]
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
/// 仅在需要时才加载字体数据，而不是将其存储在内存中
/// 对于“FontSettings”对象的整个生命周期。
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

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
