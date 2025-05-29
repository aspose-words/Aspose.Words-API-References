---
title: Border.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words for .NET
description: 探索 Border TintAndShade，轻松调整色彩亮度，只需简单的双倍数值，即可获得惊艳的设计效果。非常适合您的创意项目！
type: docs
weight: 80
url: /zh/net/aspose.words/border/tintandshade/
---
## Border.TintAndShade property

获取或设置使颜色变亮或变暗的双精度值。

```csharp
public double TintAndShade { get; set; }
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentOutOfRangeException | 如果您尝试将此属性设置为小于 -1 或大于 1 的值，则会抛出。 |
| InvalidOperationException | 如果使用非主题颜色为 Border 对象设置此属性，则会引发异常。 |

## 评论

该属性的允许值范围是从 -1（最暗）到 1（最亮）。 零 (0) 表示中性。

## 例子

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

* class [Border](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
