---
title: PageBorderDistanceFrom Enum
linktitle: PageBorderDistanceFrom
articleTitle: PageBorderDistanceFrom
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.PageBorderDistanceFrom 枚举，实现精确的页面边框定位。通过优化页边距定位，增强文档格式。
type: docs
weight: 5080
url: /zh/net/aspose.words/pageborderdistancefrom/
---
## PageBorderDistanceFrom enumeration

指定页面边框相对于页边距的位置。

```csharp
public enum PageBorderDistanceFrom
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Text | `0` | 边框位置从页边距开始测量。 |
| PageEdge | `1` | 边框位置从页面边缘测量。 |

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

* class [PageSetup](../pagesetup/)
* property [BorderDistanceFrom](../pagesetup/borderdistancefrom/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
