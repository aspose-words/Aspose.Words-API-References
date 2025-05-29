---
title: Document.PageCount
linktitle: PageCount
articleTitle: PageCount
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Document PageCount, которое отображает общее количество страниц на основе последнего макета, обеспечивая точное управление документами и аналитику.
type: docs
weight: 330
url: /ru/net/aspose.words/document/pagecount/
---
## Document.PageCount property

Возвращает количество страниц в документе, рассчитанное с помощью последней операции макета страницы.

```csharp
public int PageCount { get; }
```

## Примеры

Показывает, как подсчитать количество страниц в документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 3");

// Проверьте ожидаемое количество страниц документа.
Assert.AreEqual(3, doc.PageCount);

// Получение свойства PageCount вызвало макет страницы документа для расчета значения.
// Эту операцию не нужно будет повторять при преобразовании документа в формат сохранения с фиксированным размером страницы,
// например .pdf. Так вы сэкономите время, особенно с более сложными документами.
doc.Save(ArtifactsDir + "Document.GetPageCount.pdf");
```

### Смотрите также

* method [UpdatePageLayout](../updatepagelayout/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
