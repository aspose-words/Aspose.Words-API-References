---
title: PageBorderAppliesTo Enum
linktitle: PageBorderAppliesTo
articleTitle: PageBorderAppliesTo
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.PageBorderAppliesTo 枚举来控制跨特定页面的页面边框打印，以增强文档格式。
type: docs
weight: 5070
url: /zh/net/aspose.words/pageborderappliesto/
---
## PageBorderAppliesTo enumeration

指定打印页面边框的页面。

```csharp
public enum PageBorderAppliesTo
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| AllPages | `0` | 页面边框显示在该部分的所有页面上。 |
| FirstPage | `1` | 页面边框仅显示在该部分的第一页。 |
| OtherPages | `2` | 页面边框显示在除该部分第一页之外的所有页面上。 |

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
* property [BorderAppliesTo](../pagesetup/borderappliesto/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
