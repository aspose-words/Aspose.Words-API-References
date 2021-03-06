---
title: Shadow
second_title: Aspose.Words for .NET API 参考
description: 获取或设置边框是否有阴影的值
type: docs
weight: 110
url: /zh/net/aspose.words/bordercollection/shadow/
---
## BorderCollection.Shadow property

获取或设置边框是否有阴影的值。

```csharp
public bool Shadow { get; set; }
```

### 评论

从集合中的第一个边框获取值。

设置集合中所有边框的值，不包括对角线边框。

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

* class [BorderCollection](../../bordercollection)
* 命名空间 [Aspose.Words](../../bordercollection)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
