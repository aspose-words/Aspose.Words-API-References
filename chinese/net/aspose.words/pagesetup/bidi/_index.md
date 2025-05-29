---
title: PageSetup.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words for .NET
description: 探索 PageSetup Bidi 属性，实现无缝双向文本格式化。通过复杂脚本支持增强文档的可读性！
type: docs
weight: 10
url: /zh/net/aspose.words/pagesetup/bidi/
---
## PageSetup.Bidi property

指定此部分包含双向（复杂脚本）文本。

```csharp
public bool Bidi { get; set; }
```

## 评论

什么时候`真的`，此部分中的列从右到左布局。

## 例子

展示如何设置某一部分中文本列的顺序。

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextColumns.SetCount(3);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Write("Column 2.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Write("Column 3.");

// 将“Bidi”属性设置为“true”以从页面右侧开始排列列。
// 列的顺序将与从右到左的文本方向相匹配。
// 将“Bidi”属性设置为“false”以从页面左侧开始排列列。
// 列的顺序将与从左到右的文本方向相匹配。
pageSetup.Bidi = reverseColumns;

doc.Save(ArtifactsDir + "PageSetup.Bidi.docx");
```

### 也可以看看

* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
