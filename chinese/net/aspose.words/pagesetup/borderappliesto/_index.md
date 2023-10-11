---
title: PageSetup.BorderAppliesTo
second_title: Aspose.Words for .NET API 参考
description: PageSetup 财产. 指定在哪些页面上打印页面边框
type: docs
weight: 30
url: /zh/net/aspose.words/pagesetup/borderappliesto/
---
## PageSetup.BorderAppliesTo property

指定在哪些页面上打印页面边框。

```csharp
public PageBorderAppliesTo BorderAppliesTo { get; set; }
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

* enum [PageBorderAppliesTo](../../pageborderappliesto/)
* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../pagesetup/)
* 部件 [Aspose.Words](../../../)


