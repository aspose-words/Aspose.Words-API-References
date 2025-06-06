---
title: Font Class
linktitle: Font
articleTitle: Font
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Font 类，它具有名称、大小和颜色等基本字体属性，可增强文档格式和设计。
type: docs
weight: 3240
url: /zh/net/aspose.words/font/
---
## Font class

包含对象的字体属性（字体名称、字体大小、颜色等）。

要了解更多信息，请访问[使用字体](https://docs.aspose.com/words/net/working-with-fonts/)文档文章。

```csharp
public class Font
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AllCaps](../../aspose.words/font/allcaps/) { get; set; } | 如果字体格式为全部大写字母，则为真。 |
| [AutoColor](../../aspose.words/font/autocolor/) { get; } | 返回用于“自动颜色”的文本的当前计算颜色（黑色或白色）。 如果颜色不是“自动”，则返回[`Color`](./color/). |
| [Bidi](../../aspose.words/font/bidi/) { get; set; } | 指定此运行的内容是否应具有从右到左的特性。 |
| [Bold](../../aspose.words/font/bold/) { get; set; } | 如果字体格式为粗体，则为真。 |
| [BoldBi](../../aspose.words/font/boldbi/) { get; set; } | 如果从右到左的文本被格式化为粗体，则为真。 |
| [Border](../../aspose.words/font/border/) { get; } | 返回[`Border`](../border/)指定字体边框的对象。 |
| [Color](../../aspose.words/font/color/) { get; set; } | 获取或设置字体的颜色。 |
| [ComplexScript](../../aspose.words/font/complexscript/) { get; set; } | 指定在确定此运行的格式时，是否应将此运行的内容视为复杂脚本文本，而不管其 Unicode 字符值如何。 |
| [DoubleStrikeThrough](../../aspose.words/font/doublestrikethrough/) { get; set; } | 如果字体格式为双删除线文本，则为真。 |
| [Emboss](../../aspose.words/font/emboss/) { get; set; } | 如果字体格式为浮雕，则为真。 |
| [EmphasisMark](../../aspose.words/font/emphasismark/) { get; set; } | 获取或设置应用于此格式的强调符号。 |
| [Engrave](../../aspose.words/font/engrave/) { get; set; } | 如果字体格式为雕刻，则为真。 |
| [Fill](../../aspose.words/font/fill/) { get; } | 获取填充格式`Font`. |
| [Hidden](../../aspose.words/font/hidden/) { get; set; } | 如果字体格式为隐藏文本，则为真。 |
| [HighlightColor](../../aspose.words/font/highlightcolor/) { get; set; } | 获取或设置突出显示（标记）颜色。 |
| [Italic](../../aspose.words/font/italic/) { get; set; } | 如果字体格式为斜体，则为真。 |
| [ItalicBi](../../aspose.words/font/italicbi/) { get; set; } | 如果从右到左的文本格式化为斜体，则为真。 |
| [Kerning](../../aspose.words/font/kerning/) { get; set; } | 获取或设置字距调整开始时的字体大小。 |
| [LineSpacing](../../aspose.words/font/linespacing/) { get; } | 返回此字体的行距（以点为单位）。 |
| [LocaleId](../../aspose.words/font/localeid/) { get; set; } | 获取或设置格式化字符的区域标识符（语言）。 |
| [LocaleIdBi](../../aspose.words/font/localeidbi/) { get; set; } | 获取或设置格式化从右到左字符的区域设置标识符（语言）。 |
| [LocaleIdFarEast](../../aspose.words/font/localeidfareast/) { get; set; } | 获取或设置格式化亚洲字符的区域设置标识符（语言）。 |
| [Name](../../aspose.words/font/name/) { get; set; } | 获取或设置字体的名称。 |
| [NameAscii](../../aspose.words/font/nameascii/) { get; set; } | 返回或设置用于拉丁文本（字符代码从 0（零）到 127 的字符）的字体。 |
| [NameBi](../../aspose.words/font/namebi/) { get; set; } | 返回或设置从右到左语言文档中的字体名称。 |
| [NameFarEast](../../aspose.words/font/namefareast/) { get; set; } | 返回或设置东亚字体名称。 |
| [NameOther](../../aspose.words/font/nameother/) { get; set; } | 返回或设置字符代码从 128 到 255 的字符使用的字体。 |
| [NoProofing](../../aspose.words/font/noproofing/) { get; set; } | 当格式化字符不需要进行拼写检查时为真。 |
| [NumberSpacing](../../aspose.words/font/numberspacing/) { get; set; } | 获取或设置所显示数字的间距类型。 |
| [Outline](../../aspose.words/font/outline/) { get; set; } | 如果字体格式为轮廓，则为真。 |
| [Position](../../aspose.words/font/position/) { get; set; } | 获取或设置文本相对于基线的位置（以点为单位）。 正数升高文本，负数降低文本。 |
| [Scaling](../../aspose.words/font/scaling/) { get; set; } | 获取或设置字符宽度缩放百分比。 |
| [Shading](../../aspose.words/font/shading/) { get; } | 返回[`Shading`](../shading/)引用字体阴影格式的对象。 |
| [Shadow](../../aspose.words/font/shadow/) { get; set; } | 如果字体格式为阴影，则为真。 |
| [Size](../../aspose.words/font/size/) { get; set; } | 获取或设置字体大小（以磅为单位）。 |
| [SizeBi](../../aspose.words/font/sizebi/) { get; set; } | 获取或设置从右到左文档中使用的字体大小（以磅为单位）。 |
| [SmallCaps](../../aspose.words/font/smallcaps/) { get; set; } | 如果字体格式为小写大写字母，则为真。 |
| [SnapToGrid](../../aspose.words/font/snaptogrid/) { get; set; } | 指定当前字体在布局时是否应使用文档网格每行字符设置 。 |
| [Spacing](../../aspose.words/font/spacing/) { get; set; } | 返回或设置字符之间的间距（以点为单位）。 |
| [StrikeThrough](../../aspose.words/font/strikethrough/) { get; set; } | 如果字体格式为删除线文本，则为真。 |
| [Style](../../aspose.words/font/style/) { get; set; } | 获取或设置应用于此格式的字符样式。 |
| [StyleIdentifier](../../aspose.words/font/styleidentifier/) { get; set; } | 获取或设置应用于此格式的字符样式的区域设置独立样式标识符。 |
| [StyleName](../../aspose.words/font/stylename/) { get; set; } | 获取或设置应用于此格式的字符样式的名称。 |
| [Subscript](../../aspose.words/font/subscript/) { get; set; } | 如果字体格式为下标，则为真。 |
| [Superscript](../../aspose.words/font/superscript/) { get; set; } | 如果字体格式为上标，则为真。 |
| [TextEffect](../../aspose.words/font/texteffect/) { get; set; } | 获取或设置字体动画效果。 |
| [ThemeColor](../../aspose.words/font/themecolor/) { get; set; } | 获取或设置与此关联的应用配色方案中的主题颜色`Font`对象. |
| [ThemeFont](../../aspose.words/font/themefont/) { get; set; } | 获取或设置与此关联的应用字体方案中的主题字体`Font`对象. |
| [ThemeFontAscii](../../aspose.words/font/themefontascii/) { get; set; } | 获取或设置与此关联的应用字体方案中用于拉丁文本（字符代码从 0（零）到 127 的字符）的主题字体 `Font`对象. |
| [ThemeFontBi](../../aspose.words/font/themefontbi/) { get; set; } | 获取或设置与此关联的应用字体方案中的主题字体`Font`从右到左语言文档中的 object 。 |
| [ThemeFontFarEast](../../aspose.words/font/themefontfareast/) { get; set; } | 获取或设置与此关联的应用字体方案中的东亚主题字体`Font`对象. |
| [ThemeFontOther](../../aspose.words/font/themefontother/) { get; set; } | 获取或设置与此关联的应用字体方案中字符代码从 128 到 255 的字符所使用的主题字体`Font`对象. |
| [TintAndShade](../../aspose.words/font/tintandshade/) { get; set; } | 获取或设置使颜色变亮或变暗的双精度值。 |
| [Underline](../../aspose.words/font/underline/) { get; set; } | 获取或设置应用于字体的下划线类型。 |
| [UnderlineColor](../../aspose.words/font/underlinecolor/) { get; set; } | 获取或设置应用于字体的下划线的颜色。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [ClearFormatting](../../aspose.words/font/clearformatting/)() | 重置为默认字体格式。 |
| [HasDmlEffect](../../aspose.words/font/hasdmleffect/)(*[TextDmlEffect](../textdmleffect/)*) | 检查是否应用了特定的 DrawingML 文本效果。 |

## 评论

您无需创建`Font`直接使用类。你只需使用 `Font`访问各种对象的字体属性，例如[`Run`](../run/) , [`Paragraph`](../paragraph/)，[`Style`](../style/)，[`DocumentBuilder`](../documentbuilder/)。

## 例子

展示如何使用字体属性来格式化文本。

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

展示如何将带边框的字符串插入文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

展示如何创建和使用具有列表格式的段落样式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建自定义段落样式。
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// 创建一个列表并确保使用此样式的段落将使用此列表。
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// 将段落样式应用到文档构建器的当前段落，然后添加一些文本。
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// 将文档构建器的样式更改为没有列表格式的样式并编写另一个段落。
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
