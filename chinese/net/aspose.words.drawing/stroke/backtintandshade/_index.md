---
title: Stroke.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: Aspose.Words for .NET
description: 使用 Stroke BackTintAndShade 轻松调整描边背景颜色。控制明暗度，打造完美的设计效果。
type: docs
weight: 30
url: /zh/net/aspose.words.drawing/stroke/backtintandshade/
---
## Stroke.BackTintAndShade property

获取或设置使描边背景颜色变亮或变暗的双精度值。

```csharp
public double BackTintAndShade { get; set; }
```

## 评论

此属性的允许值范围为 -1（最暗）到 1（最亮）。 零 (0) 表示中性色。尝试将此属性设置为小于 -1 或大于 1 的值会导致ArgumentOutOfRangeException。

## 例子

展示如何设置主题颜色、色调和阴影。

```csharp
Document doc = new Document(MyDir + "Stroke gradient outline.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;
stroke.BackThemeColor = ThemeColor.Dark2;
stroke.BackTintAndShade = 0.2d;

doc.Save(ArtifactsDir + "Shape.StrokeBackThemeColors.docx");
```

### 也可以看看

* class [Stroke](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
