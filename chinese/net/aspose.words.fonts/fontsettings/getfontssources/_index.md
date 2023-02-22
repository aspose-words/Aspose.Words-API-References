---
title: FontSettings.GetFontsSources
second_title: Aspose.Words for .NET API 参考
description: FontSettings 方法. 获取数组的副本其中包含 Aspose.Words 查找 TrueType 字体的源列表
type: docs
weight: 50
url: /zh/net/aspose.words.fonts/fontsettings/getfontssources/
---
## FontSettings.GetFontsSources method

获取数组的副本，其中包含 Aspose.Words 查找 TrueType 字体的源列表。

```csharp
public FontSourceBase[] GetFontsSources()
```

### 返回值

当前字体源的副本。

### 评论

返回值是 Aspose.Words 使用的数据的副本。如果您更改返回数组中的 entries ，它将不会影响文档呈现。要指定新字体 sources 使用[`SetFontsSources`](../setfontssources/)方法。

### 例子

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
* 命名空间 [Aspose.Words.Fonts](../../fontsettings/)
* 部件 [Aspose.Words](../../../)


