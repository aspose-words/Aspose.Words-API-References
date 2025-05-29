---
title: Shading.ForegroundPatternThemeColor
linktitle: ForegroundPatternThemeColor
articleTitle: ForegroundPatternThemeColor
second_title: Aspose.Words for .NET
description: 了解如何自定义 Shading ForegroundPatternThemeColor 属性以增强设计的配色方案并提升视觉吸引力。
type: docs
weight: 50
url: /zh/net/aspose.words/shading/foregroundpatternthemecolor/
---
## Shading.ForegroundPatternThemeColor property

获取或设置与此关联的应用配色方案中的前景色图案主题颜色[`Shading`](../)对象.

```csharp
public ThemeColor ForegroundPatternThemeColor { get; set; }
```

## 例子

展示如何设置阴影纹理的前景色和背景色。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shading shading = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Shading;
shading.Texture = TextureIndex.Texture12Pt5Percent;
shading.ForegroundPatternThemeColor = ThemeColor.Dark1;
shading.BackgroundPatternThemeColor = ThemeColor.Dark2;

shading.ForegroundTintAndShade = 0.5;
shading.BackgroundTintAndShade = -0.2;

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Writeln("Foreground and background pattern colors for shading texture.");

doc.Save(ArtifactsDir + "Font.ForegroundAndBackground.docx");
```

### 也可以看看

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Shading](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
