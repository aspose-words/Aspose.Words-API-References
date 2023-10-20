---
title: FontSettings.SetFontsFolders
linktitle: SetFontsFolders
articleTitle: SetFontsFolders
second_title: 用于 .NET 的 Aspose.Words
description: FontSettings SetFontsFolders 方法. 设置 Aspose.Words 在渲染文档或嵌入字体时查找 TrueType 字体的文件夹 在 C#.
type: docs
weight: 90
url: /zh/net/aspose.words.fonts/fontsettings/setfontsfolders/
---
## FontSettings.SetFontsFolders method

设置 Aspose.Words 在渲染文档或嵌入字体时查找 TrueType 字体的文件夹。

```csharp
public void SetFontsFolders(string[] fontsFolders, bool recursive)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontsFolders | String[] | 包含 TrueType 字体的文件夹数组。 |
| recursive | Boolean | True 以递归方式扫描指定文件夹中的字体。 |

## 评论

默认情况下，Aspose.Words 会查找安装到系统中的字体。

设置此属性会重置所有先前加载的字体的缓存。

## 例子

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

* class [FontSettings](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
