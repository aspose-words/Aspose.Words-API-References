---
title: PdfLoadOptions.SkipPdfImages
second_title: Aspose.Words for .NET API 参考
description: PdfLoadOptions 财产. 获取或设置指示加载 PDF 文档时是否必须跳过图像的标志默认为错误的.
type: docs
weight: 40
url: /zh/net/aspose.words.loading/pdfloadoptions/skippdfimages/
---
## PdfLoadOptions.SkipPdfImages property

获取或设置指示加载 PDF 文档时是否必须跳过图像的标志。默认为`错误的`.

```csharp
public bool SkipPdfImages { get; set; }
```

### 例子

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
* 命名空间 [Aspose.Words.Loading](../../pdfloadoptions/)
* 部件 [Aspose.Words](../../../)


