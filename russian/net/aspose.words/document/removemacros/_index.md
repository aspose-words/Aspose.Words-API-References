---
title: Document.RemoveMacros
linktitle: RemoveMacros
articleTitle: RemoveMacros
second_title: Aspose.Words для .NET
description: С легкостью удаляйте все макросы, панели инструментов и пользовательские настройки команд из проекта VBA с помощью метода Document RemoveMacros, чтобы сделать документ более чистым.
type: docs
weight: 720
url: /ru/net/aspose.words/document/removemacros/
---
## Document.RemoveMacros method

Удаляет все макросы (проект VBA), а также панели инструментов и настройки команд из документа.

```csharp
public void RemoveMacros()
```

## Примечания

Удалив все макросы из документа, вы можете быть уверены в том, что документ не содержит макровирусов.

## Примеры

Показывает, как удалить все макросы из документа.

```csharp
Document doc = new Document(MyDir + "Macro.docm");

Assert.IsTrue(doc.HasMacros);
Assert.AreEqual("Project", doc.VbaProject.Name);

// Удалить проект VBA документа вместе со всеми его макросами.
doc.RemoveMacros();

Assert.IsFalse(doc.HasMacros);
Assert.Null(doc.VbaProject);
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
