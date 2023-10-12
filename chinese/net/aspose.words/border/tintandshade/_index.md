---
title: Border.TintAndShade
second_title: Aspose.Words for .NET API 参考
description: Border 财产. 获取或设置使颜色变亮或变暗的双精度值
type: docs
weight: 80
url: /zh/net/aspose.words/border/tintandshade/
---
## Border.TintAndShade property

获取或设置使颜色变亮或变暗的双精度值。

```csharp
public double TintAndShade { get; set; }
```

### 评论

此属性允许的值范围为 -1（最暗）到 1（最亮）。 零 (0) 为中性。尝试将此属性设置为小于 -1 或大于 1 的值会导致ArgumentOutOfRangeException。

为具有非主题 color 的 Border 对象设置此属性会导致InvalidOperationException。

### 例子

演示如何插入带有上边框的段落。

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
* 命名空间 [Aspose.Words](../../border/)
* 部件 [Aspose.Words](../../../)


