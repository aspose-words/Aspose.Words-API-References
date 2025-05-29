---
title: BuiltInDocumentProperties.SharedDocument
linktitle: SharedDocument
articleTitle: SharedDocument
second_title: Aspose.Words для .NET
description: Откройте для себя функцию BuiltInDocumentProperties SharedDocument, которая показывает, является ли ваш документ общим, что улучшает совместную работу и доступность.
type: docs
weight: 280
url: /ru/net/aspose.words.properties/builtindocumentproperties/shareddocument/
---
## BuiltInDocumentProperties.SharedDocument property

Указывает, является ли документ общим документом.

```csharp
public bool SharedDocument { get; }
```

## Примечания

Aspose.Words не обновляет это свойство.

## Примеры

Показывает, как получить расширенные свойства.

```csharp
Document doc = new Document(MyDir + "Extended properties.docx");
Assert.IsTrue(doc.BuiltInDocumentProperties.ScaleCrop);
Assert.IsTrue(doc.BuiltInDocumentProperties.SharedDocument);
Assert.IsTrue(doc.BuiltInDocumentProperties.HyperlinksChanged);
```

### Смотрите также

* class [BuiltInDocumentProperties](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)
