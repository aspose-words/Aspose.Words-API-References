---
title: Shading.ForegroundTintAndShade
linktitle: ForegroundTintAndShade
articleTitle: ForegroundTintAndShade
second_title: 用于 .NET 的 Aspose.Words
description: Shading ForegroundTintAndShade 财产. 获取或设置一个双精度值该值使前景色主题颜色变亮或变暗 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words/shading/foregroundtintandshade/
---
## Shading.ForegroundTintAndShade property

获取或设置一个双精度值，该值使前景色主题颜色变亮或变暗。

```csharp
public double ForegroundTintAndShade { get; set; }
```

## 评论

此属性允许的值范围为 -1（最暗）到 1（最亮）。 零 (0) 为中性。尝试将此属性设置为小于 -1 或大于 1 的值会导致ArgumentOutOfRangeException。

为具有非主题颜色 的着色对象设置此属性会导致InvalidOperationException。

## 例子

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

* class [Shading](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
