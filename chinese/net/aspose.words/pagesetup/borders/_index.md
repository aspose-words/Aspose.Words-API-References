---
title: PageSetup.Borders
linktitle: Borders
articleTitle: Borders
second_title: 用于 .NET 的 Aspose.Words
description: PageSetup Borders 财产. 获取页面边框的集合 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words/pagesetup/borders/
---
## PageSetup.Borders property

获取页面边框的集合。

```csharp
public BorderCollection Borders { get; }
```

## 例子

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

* class [BorderCollection](../../bordercollection/)
* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
