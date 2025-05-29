---
title: PageSetup.BorderAppliesTo
linktitle: BorderAppliesTo
articleTitle: BorderAppliesTo
second_title: Aspose.Words for .NET
description: 了解 PageSetup BorderAppliesTo 属性如何通过控制页面边框打印来增强文档布局，从而获得精美、专业的外观。
type: docs
weight: 30
url: /zh/net/aspose.words/pagesetup/borderappliesto/
---
## PageSetup.BorderAppliesTo property

指定打印页面边框的页面。

```csharp
public PageBorderAppliesTo BorderAppliesTo { get; set; }
```

## 例子

展示如何在首页顶部创建宽蓝色带状边框。

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
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
