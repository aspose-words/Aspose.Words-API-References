---
title: FontSettings.SetFontsFolder
linktitle: SetFontsFolder
articleTitle: SetFontsFolder
second_title: Aspose.Words for .NET
description: 了解如何使用 SetFontsFolder 方法在 Aspose.Words 中指定 TrueType 字体目录，增强文档渲染和字体嵌入。
type: docs
weight: 80
url: /zh/net/aspose.words.fonts/fontsettings/setfontsfolder/
---
## FontSettings.SetFontsFolder method

设置 Aspose.Words 在渲染文档或嵌入字体时查找 TrueType 字体的文件夹。 这是[`SetFontsFolders`](../setfontsfolders/)仅设置一个字体目录。

```csharp
public void SetFontsFolder(string fontFolder, bool recursive)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontFolder | String | 包含 TrueType 字体的文件夹。 |
| recursive | Boolean | 为 True，则以递归方式扫描指定文件夹中的字体。 |

## 例子

展示如何设置字体源目录。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arvo";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// 我们的字体源不包含我们用于此文档文本的字体。
// 如果我们在呈现此文档时使用这些字体设置，
// Aspose.Words 将对具有 Aspose.Words 无法找到的字体的文本应用后备字体。
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// 默认字体源缺少我们在本文档中使用的两种字体。
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// 使用“SetFontsFolder”方法设置一个目录作为新字体源。
// 传递“false”作为“递归”参数以包含目录中所有字体文件的字体
// 我们传递了第一个参数，但没有在该目录的任何子文件夹中包含任何字体。
// 传递“true”作为“递归”参数，以包含我们传递的目录中的所有字体文件
// 在第一个参数中，以及其子目录中的所有字体。
FontSettings.DefaultInstance.SetFontsFolder(FontsDir, recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// “Amethysta”字体位于字体目录的子文件夹中。
if (recursive)
{
    Assert.AreEqual(25, newFontSources[0].GetAvailableFonts().Count);
    Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}
else
{
    Assert.AreEqual(18, newFontSources[0].GetAvailableFonts().Count);
    Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolder.pdf");

// 恢复原始字体源。
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### 也可以看看

* class [FontSettings](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
