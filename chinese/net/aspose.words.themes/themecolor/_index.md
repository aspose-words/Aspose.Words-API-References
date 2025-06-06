---
title: ThemeColor Enum
linktitle: ThemeColor
articleTitle: ThemeColor
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words ThemeColor 枚举，使用鲜艳的色彩自定义文档主题，增强文档的视觉吸引力和专业性。
type: docs
weight: 7320
url: /zh/net/aspose.words.themes/themecolor/
---
## ThemeColor enumeration

指定文档主题的主题颜色。

要了解更多信息，请访问[使用样式和主题](https://docs.aspose.com/words/net/working-with-styles-and-themes/)文档文章。

```csharp
public enum ThemeColor
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `-1` | 无颜色。 |
| Dark1 | `0` | 深色主色 1. |
| Light1 | `1` | 浅主色 1. |
| Dark2 | `2` | 深色主色 2. |
| Light2 | `3` | 浅主色 2. |
| Accent1 | `4` | 强调色 1. |
| Accent2 | `5` | 强调色 2. |
| Accent3 | `6` | 强调色 3. |
| Accent4 | `7` | 强调色 4. |
| Accent5 | `8` | 强调色 5. |
| Accent6 | `9` | 强调色 6. |
| Hyperlink | `10` | 超链接颜色. |
| FollowedHyperlink | `11` | 所关注的超链接颜色。 |
| Text1 | `12` | 文本颜色 1. |
| Text2 | `13` | 文本颜色 2. |
| Background1 | `14` | 背景颜色 1. |
| Background2 | `15` | 背景颜色 2. |

## 评论

指定的主题颜色是对预定义主题颜色之一的引用，位于 文档的主题部分，允许在文档中集中设置颜色信息。

## 例子

展示如何创建和使用主题风格。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// 使用主题字体属性创建一些样式。
Style style = doc.Styles.Add(StyleType.Paragraph, "ThemedStyle");
style.Font.ThemeFont = ThemeFont.Major;
style.Font.ThemeColor = ThemeColor.Accent5;
style.Font.TintAndShade = 0.3;

builder.ParagraphFormat.StyleName = "ThemedStyle";
builder.Writeln("Text with themed style");
```

展示如何使用主题字体和颜色。

```csharp
Document doc = new Document();

// 定义默认使用的语言的字体。
doc.Theme.MinorFonts.Latin = "Algerian";
doc.Theme.MinorFonts.EastAsian = "Aharoni";
doc.Theme.MinorFonts.ComplexScript = "Andalus";

Font font = doc.Styles["Normal"].Font;
Console.WriteLine("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.ThemeColor, font.Color);

// 我们可以使用主题字体和颜色代替默认值。
font.ThemeFont = ThemeFont.Minor;
font.ThemeColor = ThemeColor.Accent2;

Assert.AreEqual(ThemeFont.Minor, font.ThemeFont);
Assert.AreEqual("Algerian", font.Name);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontAscii);
Assert.AreEqual("Algerian", font.NameAscii);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontBi);
Assert.AreEqual("Andalus", font.NameBi);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontFarEast);
Assert.AreEqual("Aharoni", font.NameFarEast);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontOther);
Assert.AreEqual("Algerian", font.NameOther);

Assert.AreEqual(ThemeColor.Accent2, font.ThemeColor);
Assert.AreEqual(Color.Empty, font.Color);

// 有几种方法可以重置字体和颜色。
// 1 - 通过设置 ThemeFont.None/ThemeColor.None：
font.ThemeFont = ThemeFont.None;
font.ThemeColor = ThemeColor.None;

Assert.AreEqual(ThemeFont.None, font.ThemeFont);
Assert.AreEqual("Algerian", font.Name);

Assert.AreEqual(ThemeFont.None, font.ThemeFontAscii);
Assert.AreEqual("Algerian", font.NameAscii);

Assert.AreEqual(ThemeFont.None, font.ThemeFontBi);
Assert.AreEqual("Andalus", font.NameBi);

Assert.AreEqual(ThemeFont.None, font.ThemeFontFarEast);
Assert.AreEqual("Aharoni", font.NameFarEast);

Assert.AreEqual(ThemeFont.None, font.ThemeFontOther);
Assert.AreEqual("Algerian", font.NameOther);

Assert.AreEqual(ThemeColor.None, font.ThemeColor);
Assert.AreEqual(Color.Empty, font.Color);

// 2 - 通过设置非主题字体/颜色名称：
font.Name = "Arial";
font.Color = Color.Blue;

Assert.AreEqual(ThemeFont.None, font.ThemeFont);
Assert.AreEqual("Arial", font.Name);

Assert.AreEqual(ThemeFont.None, font.ThemeFontAscii);
Assert.AreEqual("Arial", font.NameAscii);

Assert.AreEqual(ThemeFont.None, font.ThemeFontBi);
Assert.AreEqual("Arial", font.NameBi);

Assert.AreEqual(ThemeFont.None, font.ThemeFontFarEast);
Assert.AreEqual("Arial", font.NameFarEast);

Assert.AreEqual(ThemeFont.None, font.ThemeFontOther);
Assert.AreEqual("Arial", font.NameOther);

Assert.AreEqual(ThemeColor.None, font.ThemeColor);
Assert.AreEqual(Color.Blue.ToArgb(), font.Color.ToArgb());
```

### 也可以看看

* 命名空间 [Aspose.Words.Themes](../../aspose.words.themes/)
* 部件 [Aspose.Words](../../)
