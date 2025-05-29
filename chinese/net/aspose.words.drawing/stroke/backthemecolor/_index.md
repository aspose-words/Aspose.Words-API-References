---
title: Stroke.BackThemeColor
linktitle: BackThemeColor
articleTitle: BackThemeColor
second_title: Aspose.Words for .NET
description: 使用 Stroke BackThemeColor 属性自定义你的设计。轻松设置描边背景的主题颜色，提升视觉吸引力。
type: docs
weight: 20
url: /zh/net/aspose.words.drawing/stroke/backthemecolor/
---
## Stroke.BackThemeColor property

获取或设置代表描边背景颜色的 ThemeColor 对象。

```csharp
public ThemeColor BackThemeColor { get; set; }
```

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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Stroke](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
