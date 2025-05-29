---
title: Stroke.ForeThemeColor
linktitle: ForeThemeColor
articleTitle: ForeThemeColor
second_title: Aspose.Words for .NET
description: 使用 Stroke ForeThemeColor 属性轻松管理描边的前景色。使用鲜艳的主题颜色自定义您的设计！
type: docs
weight: 140
url: /zh/net/aspose.words.drawing/stroke/forethemecolor/
---
## Stroke.ForeThemeColor property

获取或设置代表描边前景色的 ThemeColor 对象。

```csharp
public ThemeColor ForeThemeColor { get; set; }
```

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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Stroke](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
