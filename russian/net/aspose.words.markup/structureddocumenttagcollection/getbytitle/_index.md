---
title: StructuredDocumentTagCollection.GetByTitle
linktitle: GetByTitle
articleTitle: GetByTitle
second_title: Aspose.Words для .NET
description: Откройте для себя метод GetByTitle в StructuredDocumentTagCollection, который эффективно извлекает первый тег документа по заголовку для упрощения управления данными.
type: docs
weight: 50
url: /ru/net/aspose.words.markup/structureddocumenttagcollection/getbytitle/
---
## StructuredDocumentTagCollection.GetByTitle method

Возвращает первый структурированный тег документа, обнаруженный в коллекции с указанным заголовком.

```csharp
public IStructuredDocumentTag GetByTitle(string title)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| title | String | Название структурированного тега документа. |

## Примечания

Возвращает значение null, если структурированный тег документа с указанным заголовком не найден.

## Примеры

Показывает, как получить структурированный тег документа.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Получить структурированный тег документа по идентификатору.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsMultiSection);
Console.WriteLine(sdt.Title);

// Получить структурированный тег документа или ранжированный тег по заголовку.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Смотрите также

* interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* class [StructuredDocumentTagCollection](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
