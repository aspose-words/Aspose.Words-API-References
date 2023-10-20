---
title: Theme Class
linktitle: Theme
articleTitle: Theme
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Themes.Theme 班级. 代表文档主题并提供对主要主题部分的访问包括MajorFontsMinorFonts和Colors 在 C#.
type: docs
weight: 6460
url: /zh/net/aspose.words.themes/theme/
---
## Theme class

代表文档主题，并提供对主要主题部分的访问，包括[`MajorFonts`](./majorfonts/),[`MinorFonts`](./minorfonts/)和[`Colors`](./colors/)

要了解更多信息，请访问[使用样式和主题](https://docs.aspose.com/words/net/working-with-styles-and-themes/)文档文章。

```csharp
public class Theme
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [Theme](theme/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Colors](../../aspose.words.themes/theme/colors/) { get; } | 允许指定文档的主题颜色集。 |
| [MajorFonts](../../aspose.words.themes/theme/majorfonts/) { get; } | 允许指定不同语言的主要字体集。 |
| [MinorFonts](../../aspose.words.themes/theme/minorfonts/) { get; } | 允许为不同语言指定小字体集。 |

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
