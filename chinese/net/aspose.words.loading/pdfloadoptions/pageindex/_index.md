---
title: PdfLoadOptions.PageIndex
linktitle: PageIndex
articleTitle: PageIndex
second_title: Aspose.Words for .NET
description: 探索 PdfLoadOptions PageIndex。使用此灵活属性，轻松设置 PDF 阅读的起始页码。立即优化您的 PDF 处理！
type: docs
weight: 30
url: /zh/net/aspose.words.loading/pdfloadoptions/pageindex/
---
## PdfLoadOptions.PageIndex property

获取或设置要读取的第一个页面的从 0 开始的索引。默认值为 0。

```csharp
public int PageIndex { get; set; }
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
