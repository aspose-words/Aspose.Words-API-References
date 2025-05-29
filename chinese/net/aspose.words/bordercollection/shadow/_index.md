---
title: BorderCollection.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words for .NET
description: 探索 BorderCollection Shadow 属性，提升您的设计。轻松控制边框阴影，为您的项目打造现代时尚的外观！
type: docs
weight: 110
url: /zh/net/aspose.words/bordercollection/shadow/
---
## BorderCollection.Shadow property

获取或设置一个值，指示边框是否有阴影。

```csharp
public bool Shadow { get; set; }
```

## 评论

从集合中第一个边框获取值。

设置集合中除对角线边框之外的所有边框的值。

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
