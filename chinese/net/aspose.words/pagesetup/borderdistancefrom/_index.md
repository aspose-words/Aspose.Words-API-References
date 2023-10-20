---
title: PageSetup.BorderDistanceFrom
linktitle: BorderDistanceFrom
articleTitle: BorderDistanceFrom
second_title: 用于 .NET 的 Aspose.Words
description: PageSetup BorderDistanceFrom 财产. 获取或设置一个值该值指示指定的页面边框是从页面边缘还是从它周围的文本测量的 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words/pagesetup/borderdistancefrom/
---
## PageSetup.BorderDistanceFrom property

获取或设置一个值，该值指示指定的页面边框是从页面边缘还是从它周围的文本测量的。

```csharp
public PageBorderDistanceFrom BorderDistanceFrom { get; set; }
```

## 例子

展示如何在第一页的顶部创建一个宽的蓝色边框。

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

* enum [PageBorderDistanceFrom](../../pageborderdistancefrom/)
* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
