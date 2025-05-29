---
title: IStructuredDocumentTag.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words для .NET
description: Откройте для себя свойство IStructuredDocumentTag Title — определите удобное для пользователя имя для вашего SDT и улучшите ясность документа. Узнайте больше прямо сейчас!
type: docs
weight: 140
url: /ru/net/aspose.words.markup/istructureddocumenttag/title/
---
## IStructuredDocumentTag.Title property

Указывает понятное имя, связанное с этим**СДТ** . Не может быть нулевым.

```csharp
public string Title { get; set; }
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
