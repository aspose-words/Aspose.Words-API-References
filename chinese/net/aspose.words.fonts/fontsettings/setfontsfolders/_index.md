---
title: FontSettings.SetFontsFolders
linktitle: SetFontsFolders
articleTitle: SetFontsFolders
second_title: Aspose.Words for .NET
description: 了解如何使用 Aspose.Words 中的 SetFontsFolders 方法自定义 TrueType 字体位置，以实现最佳文档渲染和嵌入。
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
| recursive | Boolean | 为 True，则以递归方式扫描指定文件夹中的字体。 |

## 评论

默认情况下，Aspose.Words 会查找系统中安装的字体。

设置此属性将重置所有先前加载的字体的缓存。

## 例子

展示如何设置多个字体源目录。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// 我们的字体源不包含我们用于此文档文本的字体。
// 如果我们在呈现此文档时使用这些字体设置，
// Aspose.Words 将对具有 Aspose.Words 无法找到的字体的文本应用后备字体。
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// 默认字体源缺少我们在本文档中使用的两种字体。
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// 使用“SetFontsFolders”方法从我们作为第一个参数传递的每个字体目录创建字体源。
// 传递“false”作为“递归”参数以包含目录中所有字体文件的字体
// 我们传递了第一个参数，但不包括任何目录子文件夹中的任何字体。
// 传递“true”作为“递归”参数，以包含我们传递的目录中的所有字体文件
// 在第一个参数中，以及其子目录中的所有字体。
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// “Junction”文件夹本身不包含字体文件，但其子文件夹包含字体文件。
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
