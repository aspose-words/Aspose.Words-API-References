---
title: IStructuredDocumentTag.IsMultiSection
linktitle: IsMultiSection
articleTitle: IsMultiSection
second_title: Aspose.Words для .NET
description: Откройте для себя свойство IsMultiSection тега IStructuredDocumentTag, которое определяет, является ли ваш тег ранжированным многосекционным, улучшая организацию и функциональность документа.
type: docs
weight: 40
url: /ru/net/aspose.words.markup/istructureddocumenttag/ismultisection/
---
## IStructuredDocumentTag.IsMultiSection property

Возвращает значение true, если этот экземпляр является ранжированным (многосекционным) структурированным тегом документа.

```csharp
public bool IsMultiSection { get; }
```

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

* interface [IStructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
