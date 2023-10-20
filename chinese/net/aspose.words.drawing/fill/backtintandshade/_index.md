---
title: Fill.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: 用于 .NET 的 Aspose.Words
description: Fill BackTintAndShade 财产. 获取或设置使背景颜色变亮或变暗的双精度值 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.drawing/fill/backtintandshade/
---
## Fill.BackTintAndShade property

获取或设置使背景颜色变亮或变暗的双精度值。

```csharp
public double BackTintAndShade { get; set; }
```

## 评论

此属性允许的值在 -1（最暗）到 1（最亮）的范围内。 零 (0) 表示中性。尝试将此属性设置为小于 -1 或大于 1 的值会导致ArgumentOutOfRangeException。

## 例子

展示如何设置前景色/背景形状颜色的主题颜色。

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
