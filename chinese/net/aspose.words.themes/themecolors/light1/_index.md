---
title: ThemeColors.Light1
linktitle: Light1
articleTitle: Light1
second_title: Aspose.Words for .NET
description: 探索 ThemeColors Light1。使用充满活力的 Light 1 颜色，轻松打造清新现代的外观，适用于任何创意项目！
type: docs
weight: 110
url: /zh/net/aspose.words.themes/themecolors/light1/
---
## ThemeColors.Light1 property

指定颜色 浅 1.

```csharp
public Color Light1 { get; set; }
```

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

* class [ThemeColors](../)
* 命名空间 [Aspose.Words.Themes](../../../aspose.words.themes/)
* 部件 [Aspose.Words](../../../)
