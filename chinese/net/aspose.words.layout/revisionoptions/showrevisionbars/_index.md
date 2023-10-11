---
title: RevisionOptions.ShowRevisionBars
second_title: Aspose.Words for .NET API 参考
description: RevisionOptions 财产. 允许指定是否应在包含修订内容的行附近呈现修订栏 默认值为真的.
type: docs
weight: 180
url: /zh/net/aspose.words.layout/revisionoptions/showrevisionbars/
---
## RevisionOptions.ShowRevisionBars property

允许指定是否应在包含修订内容的行附近呈现修订栏。 默认值为`真的`.

```csharp
public bool ShowRevisionBars { get; set; }
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

* class [RevisionOptions](../)
* 命名空间 [Aspose.Words.Layout](../../revisionoptions/)
* 部件 [Aspose.Words](../../../)


