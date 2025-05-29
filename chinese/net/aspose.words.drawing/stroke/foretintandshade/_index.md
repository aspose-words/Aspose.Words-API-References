---
title: Stroke.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: Aspose.Words for .NET
description: 调整 Stroke ForeTintAndShade 属性可轻松使笔触的前景色变亮或变暗，从而增强视觉效果。
type: docs
weight: 150
url: /zh/net/aspose.words.drawing/stroke/foretintandshade/
---
## Stroke.ForeTintAndShade property

获取或设置使描边前景色变亮或变暗的双精度值。

```csharp
public double ForeTintAndShade { get; set; }
```

## 评论

此属性的允许值范围为 -1（最暗）到 1（最亮）。 零 (0) 表示中性色。尝试将此属性设置为小于 -1 或大于 1 的值会导致ArgumentOutOfRangeException。

## 例子

展示如何设置主题颜色、色调和阴影。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 100, 40);
Stroke stroke = shape.Stroke;
stroke.ForeThemeColor = ThemeColor.Dark1;
stroke.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.StrokeForeThemeColors.docx");
```

### 也可以看看

* class [Stroke](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
