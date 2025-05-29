---
title: BorderCollection.DistanceFromText
linktitle: DistanceFromText
articleTitle: DistanceFromText
second_title: Aspose.Words for .NET
description: 探索 BorderCollection DistanceFromText 属性，轻松自定义设计中文本的边框间距。轻松优化布局！
type: docs
weight: 40
url: /zh/net/aspose.words/bordercollection/distancefromtext/
---
## BorderCollection.DistanceFromText property

获取或设置边框与文本之间的距离（以磅为单位）。

```csharp
public double DistanceFromText { get; set; }
```

## 评论

获取第一条边框与文本的距离。

设置集合中所有边框（对角线边框除外）与文本的距离。

没有效果，表格单元格的边框将自动重置为零。

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
