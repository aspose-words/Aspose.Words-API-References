---
title: Document.LayoutOptions
linktitle: LayoutOptions
articleTitle: LayoutOptions
second_title: 用于 .NET 的 Aspose.Words
description: Document LayoutOptions 财产. 得到一个布局选项表示用于控制此文档的布局过程的选项的对象 在 C#.
type: docs
weight: 250
url: /zh/net/aspose.words/document/layoutoptions/
---
## Document.LayoutOptions property

得到一个**布局选项**表示用于控制此文档的布局过程的选项的对象。

```csharp
public LayoutOptions LayoutOptions { get; }
```

## 例子

显示如何在呈现的输出文档中隐藏文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// 插入隐藏文本，然后指定我们是否希望从呈现的文档中忽略它。
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

显示如何在呈现的输出文档中显示段落标记。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// 添加一些段落，然后启用段落标记以显示段落的结尾
// 渲染文档时使用 pilcrow (¶) 符号。
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

显示如何在呈现的输出文档中更改修订的外观。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入修订，然后将所有修订的颜色更改为绿色。
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

* class [LayoutOptions](../../../aspose.words.layout/layoutoptions/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
