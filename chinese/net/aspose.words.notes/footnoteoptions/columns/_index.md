---
title: FootnoteOptions.Columns
linktitle: Columns
articleTitle: Columns
second_title: Aspose.Words for .NET
description: 探索 FootnoteOptions Columns 属性，轻松使用可自定义的列布局来格式化脚注，以增强可读性和演示效果。
type: docs
weight: 10
url: /zh/net/aspose.words.notes/footnoteoptions/columns/
---
## FootnoteOptions.Columns property

指定脚注区域格式的列数。

```csharp
public int Columns { get; set; }
```

## 评论

如果此属性的值为 0，则脚注区域的列数将根据显示页面的列数进行格式化。默认值为 0。

## 例子

展示如何将脚注部分拆分为给定数量的列。

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

### 也可以看看

* class [FootnoteOptions](../)
* 命名空间 [Aspose.Words.Notes](../../../aspose.words.notes/)
* 部件 [Aspose.Words](../../../)
