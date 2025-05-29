---
title: StructuredDocumentTagCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words для .NET
description: Легко управляйте структурированными тегами документов с помощью метода RemoveAt. Быстро удаляйте теги по индексу для упрощенного редактирования документов.
type: docs
weight: 80
url: /ru/net/aspose.words.markup/structureddocumenttagcollection/removeat/
---
## StructuredDocumentTagCollection.RemoveAt method

Удаляет структурированный тег документа по указанному индексу.

```csharp
public void RemoveAt(int index)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | Int32 | Указатель коллекции. |

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
