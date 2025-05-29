---
title: Document.FontSettings
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words for .NET
description: 了解如何轻松自定义文档字体设置。使用自定义字体选项增强文档的可读性和风格。
type: docs
weight: 150
url: /zh/net/aspose.words/document/fontsettings/
---
## Document.FontSettings property

获取或设置文档字体设置。

```csharp
public FontSettings FontSettings { get; set; }
```

## 评论

此属性允许指定每个文档的字体设置。如果设置为`无效的`、默认静态字体设置 [`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/)将被使用。

默认值为`无效的`。

## 例子

显示如何设置字体替换规则。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// 默认字体源包含文档使用的第一个字体。
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// 第二种字体“Amethysta”不可用。
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// 我们可以配置一个字体替换表来确定
// Aspose.Words 将使用哪些字体来替代不可用的字体。
// 为“Amethysta”设置两种替换字体：“Arvo”和“Courier New”。
// 如果第一个替代品不可用，Aspose.Words 将尝试使用第二个替代品，依此类推。
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

 // “Amethysta” 不可用，替换规则规定第一个用作替换的字体是“Arvo”。
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

 //“Arvo”也不可用，但“Courier New”可用。
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// 输出文档将显示使用“Amethysta”字体并以“Courier New”格式显示的文本。
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
```

### 也可以看看

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
