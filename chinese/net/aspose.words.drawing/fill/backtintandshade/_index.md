---
title: Fill.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: Aspose.Words for .NET
description: 调整 BackTintAndShade 属性可以轻松地使背景颜色变亮或变暗，增强设计的视觉吸引力和用户体验。
type: docs
weight: 30
url: /zh/net/aspose.words.drawing/fill/backtintandshade/
---
## Fill.BackTintAndShade property

获取或设置使背景颜色变亮或变暗的双精度值。

```csharp
public double BackTintAndShade { get; set; }
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentOutOfRangeException | 如果将此属性设置为小于 -1 或大于 1 的值，则抛出。 |

## 评论

此属性的允许值范围是从 -1（最暗）到 1（最亮）。

零（0）是中性的。

## 例子

展示如何设置前景/背景形状颜色的主题颜色。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.RoundRectangle, 80, 80);

Fill fill = shape.Fill;
fill.ForeThemeColor = ThemeColor.Dark1;
fill.BackThemeColor = ThemeColor.Background2;

// 注意：不要使用“BackThemeColor”和“BackTintAndShade”进行字体填充。
if (fill.BackTintAndShade == 0)
    fill.BackTintAndShade = 0.2;

doc.Save(ArtifactsDir + "Shape.FillThemeColor.docx");
```

### 也可以看看

* class [Fill](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
