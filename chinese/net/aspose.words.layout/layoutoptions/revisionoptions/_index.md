---
title: LayoutOptions.RevisionOptions
second_title: Aspose.Words for .NET API 参考
description: LayoutOptions 财产. 获取修订选项
type: docs
weight: 70
url: /zh/net/aspose.words.layout/layoutoptions/revisionoptions/
---
## LayoutOptions.RevisionOptions property

获取修订选项。

```csharp
public RevisionOptions RevisionOptions { get; }
```

### 例子

演示如何更改渲染输出文档中修订的外观。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个修订版本，然后将所有修订版本的颜色更改为绿色。
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// 删除出现在每条修改行左侧的栏。
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### 也可以看看

* class [RevisionOptions](../../revisionoptions/)
* class [LayoutOptions](../)
* 命名空间 [Aspose.Words.Layout](../../layoutoptions/)
* 部件 [Aspose.Words](../../../)


