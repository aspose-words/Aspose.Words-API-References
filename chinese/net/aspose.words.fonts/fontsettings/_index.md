---
title: FontSettings
second_title: Aspose.Words for .NET API 参考
description: 指定文档的字体设置
type: docs
weight: 2740
url: /zh/net/aspose.words.fonts/fontsettings/
---
## FontSettings class

指定文档的字体设置。

```csharp
public class FontSettings
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FontSettings](fontsettings)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| static [DefaultInstance](../../aspose.words.fonts/fontsettings/defaultinstance) { get; } | 静态默认字体设置。 |
| [FallbackSettings](../../aspose.words.fonts/fontsettings/fallbacksettings) { get; } | 与字体回退机制相关的设置。 |
| [SubstitutionSettings](../../aspose.words.fonts/fontsettings/substitutionsettings) { get; } | 字体替换机制相关设置。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFontsSources](../../aspose.words.fonts/fontsettings/getfontssources)() | 获取包含 Aspose.Words 查找 TrueType 字体的源列表的数组副本。 |
| [ResetFontSources](../../aspose.words.fonts/fontsettings/resetfontsources)() | 将字体源重置为系统默认值。 |
| [SaveSearchCache](../../aspose.words.fonts/fontsettings/savesearchcache)(Stream) | 将字体搜索缓存保存到流中。 |
| [SetFontsFolder](../../aspose.words.fonts/fontsettings/setfontsfolder)(string, bool) | 设置 Aspose.Words 在渲染文档或嵌入字体时查找 TrueType 字体的文件夹。 这是[`SetFontsFolders`](./setfontsfolders)的快捷方式，用于仅设置一个字体目录。 |
| [SetFontsFolders](../../aspose.words.fonts/fontsettings/setfontsfolders)(string[], bool) | 设置 Aspose.Words 在渲染文档或嵌入字体时查找 TrueType 字体的文件夹。 |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources#setfontssources)(FontSourceBase[]) | 设置 Aspose.Words 在渲染文档或嵌入字体时查找 TrueType 字体的来源。 |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources#setfontssources_1)(FontSourceBase[], Stream) | 设置 Aspose.Words 查找 TrueType 字体的来源，并额外加载之前保存的 字体搜索缓存。 |

### 评论

Aspose.Words 使用字体设置来解析文档中的字体。字体主要在构建文档布局 或呈现为固定页面格式时得到解决。但是在加载某些格式时，Aspose.Words 也可能需要解析字体。例如，当 加载 HTML 文档时，Aspose.Words 可能会解析字体以执行字体回退。所以建议您在加载文档时在 [`LoadOptions`](../../aspose.words.loading/loadoptions)中设置字体设置。或者至少在构建布局或将文档呈现为固定页面格式之前。

默认情况下，所有文档都使用单个静态字体设置实例。它可以通过 [`DefaultInstance`](./defaultinstance)属性访问。

在任何时间从任何线程更改字体设置都是安全的。但建议您在 处理一些使用此设置的文档时不要更改字体设置。这会导致相同的字体在文档的不同部分会以不同的方式解析 。

### 例子

展示如何将字体源添加到我们现有的字体源中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// 我们的字体源不包含我们在本文档中用于文本的字体。
// 如果我们在渲染这个文档时使用这些字体设置，
// Aspose.Words 将对具有 Aspose.Words 无法找到的字体的文本应用后备字体。
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// 默认字体源缺少我们在本文档中使用的两种字体。
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// 使用“SetFontsFolders”方法从我们作为第一个参数传递的每个字体目录创建一个字体源。
// 将“false”作为“recursive”参数传递，以包含目录中所有字体文件中的字体
// 我们传入第一个参数，但不包括任何目录子文件夹中的任何字体。
// 将“true”作为“recursive”参数传递，以包含我们传递的目录中的所有字体文件
// 在第一个参数中，以及它们子目录中的所有字体。
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// “Junction”文件夹本身不包含字体文件，但有子文件夹。
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

// 恢复原始字体源。
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

显示如何设置字体源目录。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// 我们的字体源不包含我们在本文档中用于文本的字体。
// 如果我们在渲染这个文档时使用这些字体设置，
// Aspose.Words 将对具有 Aspose.Words 无法找到的字体的文本应用后备字体。
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// 默认字体源缺少我们在本文档中使用的两种字体。
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// 使用“SetFontsFolders”方法从我们作为第一个参数传递的每个字体目录创建一个字体源。
// 将“false”作为“recursive”参数传递，以包含目录中所有字体文件中的字体
// 我们传入第一个参数，但不包括任何目录子文件夹中的任何字体。
// 将“true”作为“recursive”参数传递，以包含我们传递的目录中的所有字体文件
// 在第一个参数中，以及它们子目录中的所有字体。
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// “Junction”文件夹本身不包含字体文件，但有子文件夹。
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

// 恢复原始字体源。
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

显示如何设置多个字体源目录。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// 我们的字体源不包含我们在本文档中用于文本的字体。
// 如果我们在渲染这个文档时使用这些字体设置，
// Aspose.Words 将对具有 Aspose.Words 无法找到的字体的文本应用后备字体。
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// 默认字体源缺少我们在本文档中使用的两种字体。
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// 使用“SetFontsFolders”方法从我们作为第一个参数传递的每个字体目录创建一个字体源。
// 将“false”作为“recursive”参数传递，以包含目录中所有字体文件中的字体
// 我们传入第一个参数，但不包括任何目录子文件夹中的任何字体。
// 将“true”作为“recursive”参数传递，以包含我们传递的目录中的所有字体文件
// 在第一个参数中，以及它们子目录中的所有字体。
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// “Junction”文件夹本身不包含字体文件，但有子文件夹。
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

// 恢复原始字体源。
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### 也可以看看

* 命名空间 [Aspose.Words.Fonts](../../aspose.words.fonts)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
