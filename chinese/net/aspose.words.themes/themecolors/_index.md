---
title: ThemeColors Class
linktitle: ThemeColors
articleTitle: ThemeColors
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.ThemeColors 类，它具有多功能的 12 种颜色方案，可增强文档的视觉吸引力和一致性。
type: docs
weight: 7330
url: /zh/net/aspose.words.themes/themecolors/
---
## ThemeColors class

代表包含十二种颜色的文档主题的配色方案。

`ThemeColors`对象包含六种强调色、两种深色、两种浅色 以及每种超链接和已跟踪超链接的颜色。

```csharp
public class ThemeColors
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Accent1](../../aspose.words.themes/themecolors/accent1/) { get; set; } | 指定颜色强调 1. |
| [Accent2](../../aspose.words.themes/themecolors/accent2/) { get; set; } | 指定颜色强调 2。 |
| [Accent3](../../aspose.words.themes/themecolors/accent3/) { get; set; } | 指定颜色强调 3. |
| [Accent4](../../aspose.words.themes/themecolors/accent4/) { get; set; } | 指定颜色强调 4. |
| [Accent5](../../aspose.words.themes/themecolors/accent5/) { get; set; } | 指定颜色强调 5. |
| [Accent6](../../aspose.words.themes/themecolors/accent6/) { get; set; } | 指定颜色强调 6. |
| [Dark1](../../aspose.words.themes/themecolors/dark1/) { get; set; } | 指定颜色深色 1. |
| [Dark2](../../aspose.words.themes/themecolors/dark2/) { get; set; } | 指定颜色深色 2. |
| [FollowedHyperlink](../../aspose.words.themes/themecolors/followedhyperlink/) { get; set; } | 指定单击的超链接的颜色。 |
| [Hyperlink](../../aspose.words.themes/themecolors/hyperlink/) { get; set; } | 指定超链接的颜色。 |
| [Light1](../../aspose.words.themes/themecolors/light1/) { get; set; } | 指定颜色 浅 1. |
| [Light2](../../aspose.words.themes/themecolors/light2/) { get; set; } | 指定颜色 浅 2. |

## 例子

展示如何为主题设置自定义颜色和字体。

```csharp
Document doc = new Document(MyDir + "Theme colors.docx");

// “主题”对象使我们能够访问文档主题、默认字体和颜色的来源。
Theme theme = doc.Theme;

// 某些样式，例如“标题 1”和“副标题”，将继承这些字体。
theme.MajorFonts.Latin = "Courier New";
theme.MinorFonts.Latin = "Agency FB";

// 其他语言可能也在此主题中拥有其自定义字体。
Assert.AreEqual(string.Empty, theme.MajorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MajorFonts.EastAsian);
Assert.AreEqual(string.Empty, theme.MinorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MinorFonts.EastAsian);

//“Colors”属性包含来自 Microsoft Word 的调色板，
// 在改变阴影或字体颜色时出现。
// 将自定义颜色应用到调色板，以便我们可以在 Microsoft Word 中轻松访问它们
// 例如，当我们通过“主页”->“字体”->“字体颜色”更改字体颜色时，
// 或插入一个形状，然后通过“形状格式”->“形状样式”为其设置颜色。
ThemeColors colors = theme.Colors;
colors.Dark1 = Color.MidnightBlue;
colors.Light1 = Color.PaleGreen;
colors.Dark2 = Color.Indigo;
colors.Light2 = Color.Khaki;

colors.Accent1 = Color.OrangeRed;
colors.Accent2 = Color.LightSalmon;
colors.Accent3 = Color.Yellow;
colors.Accent4 = Color.Gold;
colors.Accent5 = Color.BlueViolet;
colors.Accent6 = Color.DarkViolet;

// 在超链接被点击和未点击的状态下应用自定义颜色。
colors.Hyperlink = Color.Black;
colors.FollowedHyperlink = Color.Gray;

doc.Save(ArtifactsDir + "Themes.CustomColorsAndFonts.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Themes](../../aspose.words.themes/)
* 部件 [Aspose.Words](../../)
