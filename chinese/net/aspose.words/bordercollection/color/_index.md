---
title: BorderCollection.Color
linktitle: Color
articleTitle: Color
second_title: 用于 .NET 的 Aspose.Words
description: BorderCollection Color 财产. 获取或设置边框颜色 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words/bordercollection/color/
---
## BorderCollection.Color property

获取或设置边框颜色。

```csharp
public Color Color { get; set; }
```

## 评论

返回集合中第一个边框的颜色。

设置集合中除对角线边框之外的所有边框的颜色。

## 例子

演示如何创建带阴影的绿色波浪页面边框。

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
