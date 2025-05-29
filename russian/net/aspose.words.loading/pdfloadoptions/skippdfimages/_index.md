---
title: PdfLoadOptions.SkipPdfImages
linktitle: SkipPdfImages
articleTitle: SkipPdfImages
second_title: Aspose.Words для .NET
description: Откройте для себя свойство SkipPdfImages в PdfLoadOptions для управления загрузкой изображений в PDF-файлах. Повысьте производительность, пропуская изображения для более быстрой обработки документов.
type: docs
weight: 40
url: /ru/net/aspose.words.loading/pdfloadoptions/skippdfimages/
---
## PdfLoadOptions.SkipPdfImages property

Возвращает или задает флаг, указывающий, следует ли пропускать изображения при загрузке документа PDF. По умолчанию`ЛОЖЬ` .

```csharp
public bool SkipPdfImages { get; set; }
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
