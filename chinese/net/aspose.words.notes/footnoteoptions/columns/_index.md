---
title: FootnoteOptions.Columns
linktitle: Columns
articleTitle: Columns
second_title: 用于 .NET 的 Aspose.Words
description: FootnoteOptions Columns 财产. 指定脚注区域格式化的列数 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.notes/footnoteoptions/columns/
---
## FootnoteOptions.Columns property

指定脚注区域格式化的列数。

```csharp
public int Columns { get; set; }
```

## 评论

如果此属性的值为 0，则脚注区域的格式将基于 显示页面上的列数。默认值为 0.

## 例子

演示如何将脚注部分拆分为给定数量的列。

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

### 也可以看看

* class [FootnoteOptions](../)
* 命名空间 [Aspose.Words.Notes](../../../aspose.words.notes/)
* 部件 [Aspose.Words](../../../)
