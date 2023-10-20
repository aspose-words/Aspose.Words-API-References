---
title: Fill.BackThemeColor
linktitle: BackThemeColor
articleTitle: BackThemeColor
second_title: 用于 .NET 的 Aspose.Words
description: Fill BackThemeColor 财产. 获取或设置一个 ThemeColor 对象该对象表示填充的背景颜色 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.drawing/fill/backthemecolor/
---
## Fill.BackThemeColor property

获取或设置一个 ThemeColor 对象，该对象表示填充的背景颜色。

```csharp
public ThemeColor BackThemeColor { get; set; }
```

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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Fill](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
