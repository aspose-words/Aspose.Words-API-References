---
title: PageBorderAppliesTo Enum
linktitle: PageBorderAppliesTo
articleTitle: PageBorderAppliesTo
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.PageBorderAppliesTo 枚举. 指定在哪些页面上打印页面边框 在 C#.
type: docs
weight: 4340
url: /zh/net/aspose.words/pageborderappliesto/
---
## PageBorderAppliesTo enumeration

指定在哪些页面上打印页面边框。

```csharp
public enum PageBorderAppliesTo
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| AllPages | `0` | 页面边框显示在该部分的所有页面上。 |
| FirstPage | `1` | 页面边框仅显示在该部分的第一页上。 |
| OtherPages | `2` | 页面边框显示在除该部分的第一页之外的所有页面上。 |

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

* class [PageSetup](../pagesetup/)
* property [BorderAppliesTo](../pagesetup/borderappliesto/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
