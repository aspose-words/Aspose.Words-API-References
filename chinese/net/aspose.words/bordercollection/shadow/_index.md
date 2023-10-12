---
title: BorderCollection.Shadow
second_title: Aspose.Words for .NET API 参考
description: BorderCollection 财产. 获取或设置一个值指示边框是否有阴影
type: docs
weight: 110
url: /zh/net/aspose.words/bordercollection/shadow/
---
## BorderCollection.Shadow property

获取或设置一个值，指示边框是否有阴影。

```csharp
public bool Shadow { get; set; }
```

### 评论

获取集合中第一个边框的值。

设置集合中除对角线边框之外的所有边框的值。

### 例子

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
* 命名空间 [Aspose.Words](../../bordercollection/)
* 部件 [Aspose.Words](../../../)


