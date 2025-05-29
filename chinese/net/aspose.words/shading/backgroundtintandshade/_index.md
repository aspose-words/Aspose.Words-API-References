---
title: Shading.BackgroundTintAndShade
linktitle: BackgroundTintAndShade
articleTitle: BackgroundTintAndShade
second_title: Aspose.Words for .NET
description: 使用 BackgroundTintAndShade 属性轻松调整背景主题颜色。调亮或调暗颜色，打造完美设计！
type: docs
weight: 30
url: /zh/net/aspose.words/shading/backgroundtintandshade/
---
## Shading.BackgroundTintAndShade property

获取或设置使背景主题颜色变亮或变暗的双精度值。

```csharp
public double BackgroundTintAndShade { get; set; }
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentOutOfRangeException | 如果将此属性设置为小于 -1 或大于 1 的值，则抛出。 |
| InvalidOperationException | 如果为具有非主题颜色的着色对象设置此属性，则抛出。 |

## 评论

此属性的允许值范围是从 -1（最暗）到 1（最亮）。

零（0）是中性的。

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

* class [Shading](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
