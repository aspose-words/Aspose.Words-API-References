---
title: IStructuredDocumentTag.RemoveSelfOnly
linktitle: RemoveSelfOnly
articleTitle: RemoveSelfOnly
second_title: Aspose.Words для .NET
description: Откройте для себя метод IStructuredDocumentTag RemoveSelfOnly, позволяющий легко удалить узел SDT, сохранив его содержимое в дереве документа.
type: docs
weight: 180
url: /ru/net/aspose.words.markup/istructureddocumenttag/removeselfonly/
---
## IStructuredDocumentTag.RemoveSelfOnly method

Удаляет только сам узел SDT, но сохраняет его содержимое внутри дерева документа.

```csharp
public void RemoveSelfOnly()
```

## Примеры

Показывает, как удалить структурированный тег документа, но сохранить содержимое внутри.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

 // Эта коллекция предоставляет унифицированный интерфейс для доступа к ранжированным и неранжированным структурированным тегам.
IEnumerable<IStructuredDocumentTag> sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(5, sdts.Count());

// Здесь мы можем получить дочерние узлы из общего интерфейса ранжированных и неранжированных структурированных тегов.
foreach (IStructuredDocumentTag sdt in sdts)
    if (sdt.GetChildNodes(NodeType.Any, false).Count > 0)
        sdt.RemoveSelfOnly();

sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(0, sdts.Count());
```

### Смотрите также

* interface [IStructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
