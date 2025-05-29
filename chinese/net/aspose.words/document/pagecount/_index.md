---
title: Document.PageCount
linktitle: PageCount
articleTitle: PageCount
second_title: Aspose.Words for .NET
description: 发现文档 PageCount 属性，该属性根据最新布局显示总页数，确保准确的文档管理和洞察。
type: docs
weight: 330
url: /zh/net/aspose.words/document/pagecount/
---
## Document.PageCount property

获取最近一次页面布局操作计算出的文档页数。

```csharp
public int PageCount { get; }
```

## 例子

显示如何计算文档的页数。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 3");

// 验证文档的预期页数。
Assert.AreEqual(3, doc.PageCount);

// 获取 PageCount 属性调用文档的页面布局来计算值。
// 将文档渲染为固定页面保存格式时无需重新执行此操作，
// 例如 .pdf。这样可以节省一些时间，尤其是在处理更复杂的文档时。
doc.Save(ArtifactsDir + "Document.GetPageCount.pdf");
```

### 也可以看看

* method [UpdatePageLayout](../updatepagelayout/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
