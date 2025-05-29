---
title: PdfLoadOptions.PageIndex
linktitle: PageIndex
articleTitle: PageIndex
second_title: Aspose.Words для .NET
description: Откройте для себя PdfLoadOptions PageIndex. Легко задайте начальный индекс страницы для чтения PDF с помощью этого гибкого свойства. Оптимизируйте обработку PDF сегодня!
type: docs
weight: 30
url: /ru/net/aspose.words.loading/pdfloadoptions/pageindex/
---
## PdfLoadOptions.PageIndex property

Возвращает или задает индекс первой страницы для чтения, начинающийся с 0. По умолчанию 0.

```csharp
public int PageIndex { get; set; }
```

## Примеры

Показывает, как пропускать изображения при загрузке PDF-файлов.

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

### Смотрите также

* class [PdfLoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
