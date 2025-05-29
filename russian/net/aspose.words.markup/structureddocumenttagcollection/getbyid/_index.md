---
title: StructuredDocumentTagCollection.GetById
linktitle: GetById
articleTitle: GetById
second_title: Aspose.Words для .NET
description: Извлекайте структурированные теги документов без усилий с помощью метода GetById. Получайте быстрый доступ к данным и повышайте эффективность управления документами.
type: docs
weight: 30
url: /ru/net/aspose.words.markup/structureddocumenttagcollection/getbyid/
---
## StructuredDocumentTagCollection.GetById method

Возвращает структурированный тег документа по идентификатору.

```csharp
public IStructuredDocumentTag GetById(int id)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| id | Int32 | Идентификатор структурированного тега документа. |

## Примечания

Возвращает null, если структурированный тег документа с указанным идентификатором не найден.

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
