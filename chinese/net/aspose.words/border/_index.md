---
title: Border Class
linktitle: Border
articleTitle: Border
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Border 类，这是您在文档中自定义对象边框的首选解决方案。精准而时尚地提升您的项目！
type: docs
weight: 270
url: /zh/net/aspose.words/border/
---
## Border class

表示对象的边框。

要了解更多信息，请访问[使用文档进行编程](https://docs.aspose.com/words/net/programming-with-documents/)文档文章。

```csharp
public class Border : InternableComplexAttr
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Color](../../aspose.words/border/color/) { get; set; } | 获取或设置边框颜色。 |
| [DistanceFromText](../../aspose.words/border/distancefromtext/) { get; set; } | 获取或设置边框与文本或页面边缘的距离（以点为单位）。 |
| [IsVisible](../../aspose.words/border/isvisible/) { get; } | 返回`真的`如果[`LineStyle`](./linestyle/)不是None. |
| [LineStyle](../../aspose.words/border/linestyle/) { get; set; } | 获取或设置边框样式。 |
| [LineWidth](../../aspose.words/border/linewidth/) { get; set; } | 获取或设置边框宽度（以点为单位）。 |
| [Shadow](../../aspose.words/border/shadow/) { get; set; } | 获取或设置一个值，指示边框是否有阴影。 |
| [ThemeColor](../../aspose.words/border/themecolor/) { get; set; } | 获取或设置与此 Border 对象关联的应用配色方案中的主题颜色。 |
| [TintAndShade](../../aspose.words/border/tintandshade/) { get; set; } | 获取或设置使颜色变亮或变暗的双精度值。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [ClearFormatting](../../aspose.words/border/clearformatting/)() | 将边框属性重置为默认值。 |
| [Equals](../../aspose.words/border/equals/#equals)(*Border*) | 确定指定边框的值是否与当前边框的值相等。 |
| override [Equals](../../aspose.words/border/equals/#equals_1)(*object*) | 确定指定对象的值是否等于当前对象。 |
| override [GetHashCode](../../aspose.words/border/gethashcode/)() | 用作此类型的哈希函数。 |

## 评论

边框可应用于各种文档元素，包括段落、段落内的文本或表格单元格。

## 例子

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

演示如何插入带有顶部边框的段落。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// 仅当设置了 LineWidth 或 LineStyle 时才设置 ThemeColor。
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### 也可以看看

* class [InternableComplexAttr](../internablecomplexattr/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
