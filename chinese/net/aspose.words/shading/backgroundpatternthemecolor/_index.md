---
title: Shading.BackgroundPatternThemeColor
second_title: Aspose.Words for .NET API 参考
description: Shading 财产. 获取或设置与此关联的已应用配色方案中的背景图案主题颜色Shading对象.
type: docs
weight: 20
url: /zh/net/aspose.words/shading/backgroundpatternthemecolor/
---
## Shading.BackgroundPatternThemeColor property

获取或设置与此关联的已应用配色方案中的背景图案主题颜色[`Shading`](../)对象.

```csharp
public ThemeColor BackgroundPatternThemeColor { get; set; }
```

### 例子

演示如何设置着色纹理的前景色和背景色。

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
* 命名空间 [Aspose.Words](../../shading/)
* 部件 [Aspose.Words](../../../)


