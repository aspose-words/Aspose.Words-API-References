---
title: Border.DistanceFromText
linktitle: DistanceFromText
articleTitle: DistanceFromText
second_title: 用于 .NET 的 Aspose.Words
description: Border DistanceFromText 财产. 获取或设置边框距文本或页面边缘的距离以磅为单位 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words/border/distancefromtext/
---
## Border.DistanceFromText property

获取或设置边框距文本或页面边缘的距离（以磅为单位）。

```csharp
public double DistanceFromText { get; set; }
```

## 评论

无效，并且表格单元格的边框将自动重置为零。

## 例子

演示如何在第一页顶部创建宽蓝色带边框。

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.BorderAlwaysInFront = false;
pageSetup.BorderDistanceFrom = PageBorderDistanceFrom.PageEdge;
pageSetup.BorderAppliesTo = PageBorderAppliesTo.FirstPage;

Border border = pageSetup.Borders[BorderType.Top];
border.LineStyle = LineStyle.Single;
border.LineWidth = 30;
border.Color = Color.Blue;
border.DistanceFromText = 0;

doc.Save(ArtifactsDir + "PageSetup.PageBorderProperties.docx");
```

### 也可以看看

* class [Border](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
