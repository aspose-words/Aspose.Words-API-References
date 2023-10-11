---
title: PageSetup.BorderDistanceFrom
second_title: Aspose.Words for .NET API 参考
description: PageSetup 财产. 获取或设置一个值该值指示指定的页面边框是从页面边缘还是从其周围的文本测量
type: docs
weight: 40
url: /zh/net/aspose.words/pagesetup/borderdistancefrom/
---
## PageSetup.BorderDistanceFrom property

获取或设置一个值，该值指示指定的页面边框是从页面边缘还是从其周围的文本测量。

```csharp
public PageBorderDistanceFrom BorderDistanceFrom { get; set; }
```

### 例子

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

* enum [PageBorderDistanceFrom](../../pageborderdistancefrom/)
* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../pagesetup/)
* 部件 [Aspose.Words](../../../)


