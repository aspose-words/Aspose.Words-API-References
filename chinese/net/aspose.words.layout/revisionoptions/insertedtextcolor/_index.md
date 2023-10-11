---
title: RevisionOptions.InsertedTextColor
second_title: Aspose.Words for .NET API 参考
description: RevisionOptions 财产. 允许指定用于插入内容的颜色Insertion. 默认值为ByAuthor.
type: docs
weight: 40
url: /zh/net/aspose.words.layout/revisionoptions/insertedtextcolor/
---
## RevisionOptions.InsertedTextColor property

允许指定用于插入内容的颜色Insertion. 默认值为ByAuthor.

```csharp
public RevisionColor InsertedTextColor { get; set; }
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

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* 命名空间 [Aspose.Words.Layout](../../revisionoptions/)
* 部件 [Aspose.Words](../../../)


