---
title: Fill.ForeTintAndShade
second_title: Aspose.Words for .NET API 参考
description: Fill 财产. 获取或设置使前景色变亮或变暗的双精度值
type: docs
weight: 90
url: /zh/net/aspose.words.drawing/fill/foretintandshade/
---
## Fill.ForeTintAndShade property

获取或设置使前景色变亮或变暗的双精度值。

```csharp
public double ForeTintAndShade { get; set; }
```

### 评论

此属性允许的值在 -1（最暗）到 1（最亮）的范围内。 零 (0) 表示中性。尝试将此属性设置为小于 -1 或大于 1 的值会导致ArgumentOutOfRangeException。

### 例子

演示如何管理前景字体颜色的变亮和变暗。

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
* 命名空间 [Aspose.Words.Drawing](../../fill/)
* 部件 [Aspose.Words](../../../)


