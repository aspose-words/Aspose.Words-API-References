---
title: ThemeFonts Class
linktitle: ThemeFonts
articleTitle: ThemeFonts
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Themes.ThemeFonts 班级. 表示字体方案中的字体集合允许为不同的语言指定不同的字体LatinEastAsian和ComplexScript 在 C#.
type: docs
weight: 6500
url: /zh/net/aspose.words.themes/themefonts/
---
## ThemeFonts class

表示字体方案中的字体集合，允许为不同的语言指定不同的字体[`Latin`](./latin/),[`EastAsian`](./eastasian/)和[`ComplexScript`](./complexscript/).

要了解更多信息，请访问[使用样式和主题](https://docs.aspose.com/words/net/working-with-styles-and-themes/)文档文章。

```csharp
public class ThemeFonts
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [ComplexScript](../../aspose.words.themes/themefonts/complexscript/) { get; set; } | 指定 ComplexScript 字符的字体名称。 |
| [EastAsian](../../aspose.words.themes/themefonts/eastasian/) { get; set; } | 指定东亚字符的字体名称。 |
| [Latin](../../aspose.words.themes/themefonts/latin/) { get; set; } | 指定拉丁字符的字体名称。 |

## 例子

展示如何设置主题的自定义颜色和字体。

```csharp
Document doc = new Document(MyDir + "Theme colors.docx");

// “Theme”对象使我们能够访问文档主题，默认字体和颜色的来源。
Theme theme = doc.Theme;

// 某些样式，例如“标题1”和“副标题”，将继承这些字体。
theme.MajorFonts.Latin = "Courier New";
theme.MinorFonts.Latin = "Agency FB";

// 其他语言也可能在此主题中有其自定义字体。
Assert.AreEqual(string.Empty, theme.MajorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MajorFonts.EastAsian);
Assert.AreEqual(string.Empty, theme.MinorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MinorFonts.EastAsian);

// “Colors”属性包含 Microsoft Word 中的调色板，
// 更改阴影或字体颜色时出现。
// 将自定义颜色应用到调色板，以便我们可以在 Microsoft Word 中轻松访问它们
// 例如，当我们通过“Home”更改字体颜色时 -> “字体”-> “字体颜色”，
// 或者插入一个形状，然后通过“形状格式”为其设置颜色 -> “形状样式”。
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

// 将自定义颜色应用于已单击和未单击状态的超链接。
colors.Hyperlink = Color.Black;
colors.FollowedHyperlink = Color.Gray;

doc.Save(ArtifactsDir + "Themes.CustomColorsAndFonts.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Themes](../../aspose.words.themes/)
* 部件 [Aspose.Words](../../)
