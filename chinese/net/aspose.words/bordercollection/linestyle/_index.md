---
title: BorderCollection.LineStyle
linktitle: LineStyle
articleTitle: LineStyle
second_title: Aspose.Words for .NET
description: 探索 BorderCollection 的 LineStyle 属性，使用灵活的边框样式自定义您的设计。轻松提升项目的视觉吸引力！
type: docs
weight: 80
url: /zh/net/aspose.words/bordercollection/linestyle/
---
## BorderCollection.LineStyle property

获取或设置边框样式。

```csharp
public LineStyle LineStyle { get; set; }
```

## 评论

返回集合中第一个边框的样式。

设置集合中除对角线边框之外的所有边框的样式。

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

* enum [LineStyle](../../linestyle/)
* class [BorderCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
