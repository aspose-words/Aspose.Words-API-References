---
title: Document.RemoveMacros
linktitle: RemoveMacros
articleTitle: RemoveMacros
second_title: Aspose.Words для .NET
description: Document RemoveMacros метод. Удаляет из документа все макросы проект VBA а также панели инструментов и настройки команд на С#.
type: docs
weight: 670
url: /ru/net/aspose.words/document/removemacros/
---
## Document.RemoveMacros method

Удаляет из документа все макросы (проект VBA), а также панели инструментов и настройки команд.

```csharp
public void RemoveMacros()
```

## Примечания

Удалив все макросы из документа, вы можете гарантировать, что документ не содержит макровирусов.

## Примеры

Показывает, как удалить все макросы из документа.

```csharp
Document doc = new Document(MyDir + "Macro.docm");

Assert.IsTrue(doc.HasMacros);
Assert.AreEqual("Project", doc.VbaProject.Name);

// Удаляем проект VBA документа вместе со всеми его макросами.
doc.RemoveMacros();

Assert.IsFalse(doc.HasMacros);
Assert.Null(doc.VbaProject);
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
