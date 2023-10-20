---
title: BorderCollection.DistanceFromText
linktitle: DistanceFromText
articleTitle: DistanceFromText
second_title: 用于 .NET 的 Aspose.Words
description: BorderCollection DistanceFromText 财产. 获取或设置文本边框的距离以磅为单位 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words/bordercollection/distancefromtext/
---
## BorderCollection.DistanceFromText property

获取或设置文本边框的距离（以磅为单位）。

```csharp
public double DistanceFromText { get; set; }
```

## 评论

获取第一个边框距文本的距离。

设置集合中除对角线边框之外的所有边框与文本的距离。

没有任何效果，并且表格单元格的边框将自动重置为零。

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
