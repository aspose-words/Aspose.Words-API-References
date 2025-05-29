---
title: Document.LayoutOptions
linktitle: LayoutOptions
articleTitle: LayoutOptions
second_title: Aspose.Words for .NET
description: 探索文档布局选项 (Document LayoutOptions) 属性，有效控制文档布局。解锁灵活的设计选项，实现最佳呈现效果。
type: docs
weight: 260
url: /zh/net/aspose.words/document/layoutoptions/
---
## Document.LayoutOptions property

获得[`LayoutOptions`](../../../aspose.words.layout/layoutoptions/)表示控制此文档布局过程的选项的对象。

```csharp
public LayoutOptions LayoutOptions { get; }
```

## 例子

展示如何在渲染的输出文档中隐藏文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// 插入隐藏文本，然后指定我们是否希望从呈现的文档中省略它。
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

展示如何在渲染的输出文档中显示段落标记。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// 添加一些段落，然后启用段落标记来显示段落的结尾
// 当我们呈现文档时，使用段落标记 (¶) 符号。
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

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

* class [LayoutOptions](../../../aspose.words.layout/layoutoptions/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
