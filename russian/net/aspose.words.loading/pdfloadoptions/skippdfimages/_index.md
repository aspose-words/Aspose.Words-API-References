---
title: PdfLoadOptions.SkipPdfImages
linktitle: SkipPdfImages
articleTitle: SkipPdfImages
second_title: Aspose.Words для .NET
description: PdfLoadOptions SkipPdfImages свойство. Получает или задает флаг указывающий следует ли пропускать изображения при загрузке PDFдокумента. По умолчаниюЛОЖЬ  на С#.
type: docs
weight: 40
url: /ru/net/aspose.words.loading/pdfloadoptions/skippdfimages/
---
## PdfLoadOptions.SkipPdfImages property

Получает или задает флаг, указывающий, следует ли пропускать изображения при загрузке PDF-документа. По умолчанию`ЛОЖЬ` .

```csharp
public bool SkipPdfImages { get; set; }
```

## Примеры

Показывает, как пропускать изображения во время загрузки PDF-файлов.

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

### Смотрите также

* class [PdfLoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
