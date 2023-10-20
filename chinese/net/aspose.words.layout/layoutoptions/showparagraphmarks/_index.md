---
title: LayoutOptions.ShowParagraphMarks
linktitle: ShowParagraphMarks
articleTitle: ShowParagraphMarks
second_title: 用于 .NET 的 Aspose.Words
description: LayoutOptions ShowParagraphMarks 财产. 获取或设置是否呈现段落标记的指示 默认为错误的 在 C#.
type: docs
weight: 90
url: /zh/net/aspose.words.layout/layoutoptions/showparagraphmarks/
---
## LayoutOptions.ShowParagraphMarks property

获取或设置是否呈现段落标记的指示。 默认为`错误的`.

```csharp
public bool ShowParagraphMarks { get; set; }
```

## 例子

演示如何在渲染的输出文档中显示段落标记。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// 添加一些段落，然后启用段落标记以显示段落结尾
// 当我们渲染文档时使用 pilcrow (¶) 符号。
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

### 也可以看看

* class [LayoutOptions](../)
* 命名空间 [Aspose.Words.Layout](../../../aspose.words.layout/)
* 部件 [Aspose.Words](../../../)
