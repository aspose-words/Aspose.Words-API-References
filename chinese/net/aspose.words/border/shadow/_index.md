---
title: Border.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words for .NET
description: 探索边框阴影属性，提升您的设计！控制边框阴影效果，以惊艳的视觉效果提升您的 UI 体验。
type: docs
weight: 60
url: /zh/net/aspose.words/border/shadow/
---
## Border.Shadow property

获取或设置一个值，指示边框是否有阴影。

```csharp
public bool Shadow { get; set; }
```

## 评论

在 Microsoft Word 中，要使边框有阴影，所有四个边（左、上、右和下）的边框应具有相同的类型、宽度、颜色，并且所有边框都应将 Shadow 属性设置为`真的`。

## 例子

展示如何创建带有阴影的绿色波浪页面边框。

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
