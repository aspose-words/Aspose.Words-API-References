---
title: Border.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: 用于 .NET 的 Aspose.Words
description: Border Shadow 财产. 获取或设置边框是否有阴影的值 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words/border/shadow/
---
## Border.Shadow property

获取或设置边框是否有阴影的值。

```csharp
public bool Shadow { get; set; }
```

## 评论

在 Microsoft Word 中，要使边框具有阴影，所有四个边 （左、上、右和下）的边框都应具有相同的类型、宽度、颜色，并且都应将 Shadow 属性设置为 true。

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

* class [Border](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
