---
title: Range.StructuredDocumentTags
linktitle: StructuredDocumentTags
articleTitle: StructuredDocumentTags
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Range StructuredDocumentTags, которое предоставляет полную коллекцию структурированных тегов документа, улучшая организацию и функциональность вашего документа.
type: docs
weight: 50
url: /ru/net/aspose.words/range/structureddocumenttags/
---
## Range.StructuredDocumentTags property

Возвращает`StructuredDocumentTags` коллекция, представляющая все структурированные теги документов в диапазоне .

```csharp
public StructuredDocumentTagCollection StructuredDocumentTags { get; }
```

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

* class [StructuredDocumentTagCollection](../../../aspose.words.markup/structureddocumenttagcollection/)
* class [Range](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
