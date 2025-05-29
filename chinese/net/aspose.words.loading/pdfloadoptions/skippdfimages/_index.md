---
title: PdfLoadOptions.SkipPdfImages
linktitle: SkipPdfImages
articleTitle: SkipPdfImages
second_title: Aspose.Words for .NET
description: 探索 PdfLoadOptions 的 SkipPdfImages 属性，以控制 PDF 中的图像加载。通过跳过图像来提高性能，从而加快文档处理速度。
type: docs
weight: 40
url: /zh/net/aspose.words.loading/pdfloadoptions/skippdfimages/
---
## PdfLoadOptions.SkipPdfImages property

获取或设置标志，指示加载 PDF 文档时是否必须跳过图像。默认值为`错误的`.

```csharp
public bool SkipPdfImages { get; set; }
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
