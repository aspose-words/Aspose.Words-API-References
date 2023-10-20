---
title: PdfLoadOptions.SkipPdfImages
linktitle: SkipPdfImages
articleTitle: SkipPdfImages
second_title: 用于 .NET 的 Aspose.Words
description: PdfLoadOptions SkipPdfImages 财产. 获取或设置指示加载 PDF 文档时是否必须跳过图像的标志默认为错误的 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.loading/pdfloadoptions/skippdfimages/
---
## PdfLoadOptions.SkipPdfImages property

获取或设置指示加载 PDF 文档时是否必须跳过图像的标志。默认为`错误的`.

```csharp
public bool SkipPdfImages { get; set; }
```

## 例子

演示如何在加载 PDF 文件期间跳过图像。

```csharp
PdfLoadOptions options = new PdfLoadOptions();
options.SkipPdfImages = isSkipPdfImages;

Document doc = new Document(MyDir + "Images.pdf", options);
NodeCollection shapeCollection = doc.GetChildNodes(NodeType.Shape, true);

if (isSkipPdfImages)
{
    Assert.AreEqual(shapeCollection.Count, 0);
}
else
{
    Assert.AreNotEqual(shapeCollection.Count, 0);
}
```

### 也可以看看

* class [PdfLoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
