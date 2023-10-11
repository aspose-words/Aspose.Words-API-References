---
title: Border.Shadow
second_title: Aspose.Words for .NET API 参考
description: Border 财产. 获取或设置一个值指示边框是否有阴影
type: docs
weight: 60
url: /zh/net/aspose.words/border/shadow/
---
## Border.Shadow property

获取或设置一个值，指示边框是否有阴影。

```csharp
public bool Shadow { get; set; }
```

### 评论

在 Microsoft Word 中，要使边框具有阴影，所有四个边 （左、上、右和下）的边框应具有相同的类型、宽度、颜色，并且所有边框都应将 的 Shadow 属性设置为`真的`。

### 例子

演示如何创建带阴影的绿色波浪页面边框。

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
* 命名空间 [Aspose.Words](../../border/)
* 部件 [Aspose.Words](../../../)


