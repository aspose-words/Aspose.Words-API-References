---
title: PdfLoadOptions.PageCount
linktitle: PageCount
articleTitle: PageCount
second_title: Aspose.Words для .NET
description: Контролируйте чтение страниц с помощью свойства PageCount в PdfLoadOptions. Легко задавайте количество страниц для чтения, обеспечивая эффективную обработку документов.
type: docs
weight: 20
url: /ru/net/aspose.words.loading/pdfloadoptions/pagecount/
---
## PdfLoadOptions.PageCount property

Возвращает или задает количество страниц для чтения. По умолчанию MaxValue, что означает, что все страницы документа будут прочитаны.

```csharp
public int PageCount { get; set; }
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
