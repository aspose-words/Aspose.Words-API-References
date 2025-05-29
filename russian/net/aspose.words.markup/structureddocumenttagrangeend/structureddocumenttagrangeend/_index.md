---
title: StructuredDocumentTagRangeEnd
linktitle: StructuredDocumentTagRangeEnd
articleTitle: StructuredDocumentTagRangeEnd
second_title: Aspose.Words для .NET
description: Откройте для себя конструктор StructuredDocumentTagRangeEnd — эффективно инициализируйте диапазоны тегов документа для улучшенного управления контентом и бесшовной интеграции.
type: docs
weight: 10
url: /ru/net/aspose.words.markup/structureddocumenttagrangeend/structureddocumenttagrangeend/
---
## StructuredDocumentTagRangeEnd constructor

Инициализирует новый экземпляр**Конец диапазона тегов структурированного документа** класс.

```csharp
public StructuredDocumentTagRangeEnd(DocumentBase doc, int id)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | DocumentBase | Документ владельца. |
| id | Int32 | Идентификатор начала диапазона тегов соответствующего структурированного документа. |

## Примеры

Показывает, как создать/удалить структурированный тег документа и его содержимое.

```csharp
public void SdtRangeExtendedMethods()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("StructuredDocumentTag element");

    StructuredDocumentTagRangeStart rangeStart = InsertStructuredDocumentTagRanges(doc);

    // Удаляет тег структурированного документа с диапазоном, но сохраняет содержимое внутри.
    rangeStart.RemoveSelfOnly();

    rangeStart = (StructuredDocumentTagRangeStart)doc.GetChild(
        NodeType.StructuredDocumentTagRangeStart, 0, false);
    Assert.AreEqual(null, rangeStart);

    StructuredDocumentTagRangeEnd rangeEnd = (StructuredDocumentTagRangeEnd)doc.GetChild(
        NodeType.StructuredDocumentTagRangeEnd, 0, false);

    Assert.AreEqual(null, rangeEnd);
    Assert.AreEqual("StructuredDocumentTag element", doc.GetText().Trim());

    rangeStart = InsertStructuredDocumentTagRanges(doc);

    Node paragraphNode = rangeStart.LastOrDefault();
    Assert.AreEqual("StructuredDocumentTag element", paragraphNode?.GetText().Trim());

    // Удаляет тег структурированного документа с диапазоном и его содержимое.
    rangeStart.RemoveAllChildren();

    paragraphNode = rangeStart.LastOrDefault();
    Assert.AreEqual(null, paragraphNode?.GetText());
}

public StructuredDocumentTagRangeStart InsertStructuredDocumentTagRanges(Document doc)
{
    StructuredDocumentTagRangeStart rangeStart = new StructuredDocumentTagRangeStart(doc, SdtType.PlainText);
    StructuredDocumentTagRangeEnd rangeEnd = new StructuredDocumentTagRangeEnd(doc, rangeStart.Id);

    doc.FirstSection.Body.InsertBefore(rangeStart, doc.FirstSection.Body.FirstParagraph);
    doc.LastSection.Body.InsertAfter(rangeEnd, doc.FirstSection.Body.FirstParagraph);

    return rangeStart;
}
```

### Смотрите также

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [StructuredDocumentTagRangeEnd](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
