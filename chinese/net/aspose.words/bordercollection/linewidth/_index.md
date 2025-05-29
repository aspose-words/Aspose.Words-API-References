---
title: BorderCollection.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: Aspose.Words for .NET
description: 探索 BorderCollection LineWidth 属性，轻松调整边框宽度（以点为单位），增强设计的精确度和视觉吸引力。
type: docs
weight: 90
url: /zh/net/aspose.words/bordercollection/linewidth/
---
## BorderCollection.LineWidth property

获取或设置边框宽度（以点为单位）。

```csharp
public double LineWidth { get; set; }
```

## 评论

返回集合中第一个边框的宽度。

设置集合中除对角线边框之外的所有边框的宽度。

## 例子

展示如何创建带有阴影的绿色波浪页面边框。

```csharp
Document doc = new Document();
PageSetup pageSetup = doc.Sections[0].PageSetup;

pageSetup.Borders.LineStyle = LineStyle.DoubleWave;
pageSetup.Borders.LineWidth = 2;
pageSetup.Borders.Color = Color.Green;
pageSetup.Borders.DistanceFromText = 24;
pageSetup.Borders.Shadow = true;

doc.Save(ArtifactsDir + "PageSetup.PageBorders.docx");
```

### 也可以看看

* class [BorderCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
