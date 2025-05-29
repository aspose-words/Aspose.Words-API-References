---
title: PdfLoadOptions.PageCount
linktitle: PageCount
articleTitle: PageCount
second_title: Aspose.Words for .NET
description: 使用 PdfLoadOptions 的 PageCount 属性控制页面读取。轻松设置读取页数，确保高效的文档处理。
type: docs
weight: 20
url: /zh/net/aspose.words.loading/pdfloadoptions/pagecount/
---
## PdfLoadOptions.PageCount property

获取或设置要读取的页数。默认值为 MaxValue，表示将读取文档的所有页面。

```csharp
public int PageCount { get; set; }
```

## 例子

展示如何在加载 PDF 文件时跳过图像。

```csharp
PdfLoadOptions options = new PdfLoadOptions();
options.SkipPdfImages = isSkipPdfImages;
options.PageIndex = 0;
options.PageCount = 1;

Document doc = new Document(MyDir + "Images.pdf", options);
NodeCollection shapeCollection = doc.GetChildNodes(NodeType.Shape, true);

if (isSkipPdfImages)
    Assert.AreEqual(shapeCollection.Count, 0);
else
    Assert.AreNotEqual(shapeCollection.Count, 0);
```

### 也可以看看

* class [PdfLoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
