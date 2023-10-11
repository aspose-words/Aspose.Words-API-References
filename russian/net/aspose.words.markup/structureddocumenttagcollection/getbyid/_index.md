---
title: StructuredDocumentTagCollection.GetById
second_title: Справочник по API Aspose.Words для .NET
description: StructuredDocumentTagCollection метод. Возвращает тег структурированного документа по идентификатору.
type: docs
weight: 30
url: /ru/net/aspose.words.markup/structureddocumenttagcollection/getbyid/
---
## StructuredDocumentTagCollection.GetById method

Возвращает тег структурированного документа по идентификатору.

```csharp
public IStructuredDocumentTag GetById(int id)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| id | Int32 | Идентификатор тега структурированного документа. |

### Примечания

Возвращает значение NULL, если тег структурированного документа с указанным идентификатором не найден.

### Примеры

Показывает, как получить структурированный тег документа.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Получаем тег структурированного документа по идентификатору.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsRanged());
Console.WriteLine(sdt.Title);

// Получаем тег структурированного документа или тег с ранжированием по заголовку.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Смотрите также

* interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* class [StructuredDocumentTagCollection](../)
* пространство имен [Aspose.Words.Markup](../../structureddocumenttagcollection/)
* сборка [Aspose.Words](../../../)


