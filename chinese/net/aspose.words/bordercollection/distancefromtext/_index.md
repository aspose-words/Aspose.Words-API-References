---
title: BorderCollection.DistanceFromText
second_title: Aspose.Words for .NET API 参考
description: BorderCollection 财产. 获取或设置边框与文本的距离以点为单位
type: docs
weight: 40
url: /zh/net/aspose.words/bordercollection/distancefromtext/
---
## BorderCollection.DistanceFromText property

获取或设置边框与文本的距离，以点为单位。

```csharp
public double DistanceFromText { get; set; }
```

### 评论

获取第一个边框与文本的距离。

为集合中的所有边框设置与文本的距离，不包括对角线边框。

没有效果，表格单元格的边框将自动重置为零。

### 例子

演示如何创建带有阴影的绿色波浪页面边框。

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
* 命名空间 [Aspose.Words](../../bordercollection/)
* 部件 [Aspose.Words](../../../)


