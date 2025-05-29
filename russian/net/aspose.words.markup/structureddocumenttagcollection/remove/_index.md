---
title: StructuredDocumentTagCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words для .NET
description: С легкостью удаляйте определенные структурированные теги документов с помощью метода StructuredDocumentTagCollection Remove для упрощения управления документами.
type: docs
weight: 70
url: /ru/net/aspose.words.markup/structureddocumenttagcollection/remove/
---
## StructuredDocumentTagCollection.Remove method

Удаляет структурированный тег документа с указанным идентификатором.

```csharp
public void Remove(int id)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| id | Int32 | Идентификатор структурированного тега документа. |

## Примеры

Показывает, как удалить структурированный тег документа.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

StructuredDocumentTagCollection structuredDocumentTags = doc.Range.StructuredDocumentTags;
IStructuredDocumentTag sdt;
for (int i = 0; i < structuredDocumentTags.Count; i++)
{
    sdt = structuredDocumentTags[i];
    Console.WriteLine(sdt.Title);
}

sdt = structuredDocumentTags.GetById(1691867797);
Assert.AreEqual(1691867797, sdt.Id);

Assert.AreEqual(5, structuredDocumentTags.Count);
// Удалить структурированный тег документа по идентификатору.
structuredDocumentTags.Remove(1691867797);
// Удалить структурированный тег документа в позиции 0.
structuredDocumentTags.RemoveAt(0);
Assert.AreEqual(3, structuredDocumentTags.Count);
```

### Смотрите также

* class [StructuredDocumentTagCollection](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
