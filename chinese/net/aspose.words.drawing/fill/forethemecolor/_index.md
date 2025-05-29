---
title: Fill.ForeThemeColor
linktitle: ForeThemeColor
articleTitle: ForeThemeColor
second_title: Aspose.Words for .NET
description: 了解如何设置 ForeThemeColor 属性，使用鲜艳的填充颜色自定义设计。轻松提升项目的视觉吸引力！
type: docs
weight: 80
url: /zh/net/aspose.words.drawing/fill/forethemecolor/
---
## Fill.ForeThemeColor property

获取或设置代表填充前景色的 ThemeColor 对象。

```csharp
public ThemeColor ForeThemeColor { get; set; }
```

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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Fill](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
