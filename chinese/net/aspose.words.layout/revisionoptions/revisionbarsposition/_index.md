---
title: RevisionOptions.RevisionBarsPosition
linktitle: RevisionBarsPosition
articleTitle: RevisionBarsPosition
second_title: Aspose.Words for .NET
description: 了解如何自定义 RevisionOptions 中的 RevisionBarsPosition 属性，以增强文档的外观。默认设置为“Outside”。
type: docs
weight: 160
url: /zh/net/aspose.words.layout/revisionoptions/revisionbarsposition/
---
## RevisionOptions.RevisionBarsPosition property

获取或设置修订栏的渲染位置。 默认值为Outside.

```csharp
public HorizontalAlignment RevisionBarsPosition { get; set; }
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentOutOfRangeException | 价值观Center和Inside不允许使用 。 |

## 例子

展示如何改变渲染输出文档中修订版本的外观。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入修订，然后将所有修订的颜色更改为绿色。
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// 删除出现在每个修订行左侧的栏。
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### 也可以看看

* enum [HorizontalAlignment](../../../aspose.words.drawing/horizontalalignment/)
* class [RevisionOptions](../)
* 命名空间 [Aspose.Words.Layout](../../../aspose.words.layout/)
* 部件 [Aspose.Words](../../../)
