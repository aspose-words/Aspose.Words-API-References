---
title: IStructuredDocumentTag.IsRanged
linktitle: IsRanged
articleTitle: IsRanged
second_title: Aspose.Words для .NET
description: IStructuredDocumentTag IsRanged метод. Возвращает true если этот экземпляр является тегом структурированного документа с ранжированием на С#.
type: docs
weight: 140
url: /ru/net/aspose.words.markup/istructureddocumenttag/isranged/
---
## IStructuredDocumentTag.IsRanged method

Возвращает true, если этот экземпляр является тегом структурированного документа с ранжированием.

```csharp
public bool IsRanged()
```

## Примеры

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

* interface [IStructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
