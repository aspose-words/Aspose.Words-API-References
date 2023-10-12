---
title: StructuredDocumentTagCollection.Remove
second_title: Справочник по API Aspose.Words для .NET
description: StructuredDocumentTagCollection метод. Удаляет тег структурированного документа с указанным идентификатором.
type: docs
weight: 70
url: /ru/net/aspose.words.markup/structureddocumenttagcollection/remove/
---
## StructuredDocumentTagCollection.Remove method

Удаляет тег структурированного документа с указанным идентификатором.

```csharp
public void Remove(int id)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| id | Int32 | Идентификатор тега структурированного документа. |

### Примеры

Показывает, как удалить тег структурированного документа.

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
// Удаляем тег структурированного документа по идентификатору.
structuredDocumentTags.Remove(1691867797);
// Удаляем тег структурированного документа в позиции 0.
structuredDocumentTags.RemoveAt(0);
Assert.AreEqual(3, structuredDocumentTags.Count);
```

### Смотрите также

* class [StructuredDocumentTagCollection](../)
* пространство имен [Aspose.Words.Markup](../../structureddocumenttagcollection/)
* сборка [Aspose.Words](../../../)


