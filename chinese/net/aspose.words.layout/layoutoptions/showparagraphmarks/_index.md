---
title: LayoutOptions.ShowParagraphMarks
linktitle: ShowParagraphMarks
articleTitle: ShowParagraphMarks
second_title: Aspose.Words for .NET
description: 了解 LayoutOptions ShowParagraphMarks 属性如何通过切换段落标记的可见性来增强文本格式。立即提升您的文档清晰度！
type: docs
weight: 90
url: /zh/net/aspose.words.layout/layoutoptions/showparagraphmarks/
---
## LayoutOptions.ShowParagraphMarks property

获取或设置是否呈现段落标记的指示。 默认值为`错误的`.

```csharp
public bool ShowParagraphMarks { get; set; }
```

## 例子

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

### 也可以看看

* class [LayoutOptions](../)
* 命名空间 [Aspose.Words.Layout](../../../aspose.words.layout/)
* 部件 [Aspose.Words](../../../)
