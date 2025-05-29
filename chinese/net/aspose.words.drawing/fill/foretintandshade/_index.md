---
title: Fill.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: Aspose.Words for .NET
description: 调整 ForeTintAndShade 属性可轻松使前景色变亮或变暗，从而精确且富有创造力地增强您的设计。
type: docs
weight: 90
url: /zh/net/aspose.words.drawing/fill/foretintandshade/
---
## Fill.ForeTintAndShade property

获取或设置使前景色变亮或变暗的双精度值。

```csharp
public double ForeTintAndShade { get; set; }
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentOutOfRangeException | 如果将此属性设置为小于 -1 或大于 1 的值，则抛出。 |

## 评论

此属性的允许值范围是从 -1（最暗）到 1（最亮）。

零（0）是中性的。

## 例子

展示如何管理前景色字体颜色的变亮和变暗。

```csharp
Document doc = new Document(MyDir + "Big document.docx");

Fill textFill = doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Fill;
textFill.ForeThemeColor = ThemeColor.Accent1;
if (textFill.ForeTintAndShade == 0)
    textFill.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.FillTintAndShade.docx");
```

### 也可以看看

* class [Fill](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
