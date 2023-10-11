---
title: Document.PageCount
second_title: Справочник по API Aspose.Words для .NET
description: Document свойство. Получает количество страниц в документе рассчитанное с помощью последней операции макета страницы.
type: docs
weight: 320
url: /ru/net/aspose.words/document/pagecount/
---
## Document.PageCount property

Получает количество страниц в документе, рассчитанное с помощью последней операции макета страницы.

```csharp
public int PageCount { get; }
```

### Примеры

Показывает, как подсчитать количество страниц в документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 3");

// Проверяем ожидаемое количество страниц документа.
Assert.AreEqual(3, doc.PageCount);

// Получение свойства PageCount вызывает макет страницы документа для вычисления значения.
// Эту операцию не нужно будет повторять при рендеринге документа в фиксированный формат сохранения страницы,
// например .pdf. Таким образом, вы сможете сэкономить время, особенно при работе с более сложными документами.
doc.Save(ArtifactsDir + "Document.GetPageCount.pdf");
```

### Смотрите также

* method [UpdatePageLayout](../updatepagelayout/)
* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


