---
title: BuiltInDocumentProperties.HyperlinksChanged
linktitle: HyperlinksChanged
articleTitle: HyperlinksChanged
second_title: Aspose.Words для .NET
description: Откройте для себя свойство BuiltInDocumentProperties HyperlinksChanged, которое отслеживает изменения гиперссылок в ваших документах для улучшенного управления редактированием.
type: docs
weight: 130
url: /ru/net/aspose.words.properties/builtindocumentproperties/hyperlinkschanged/
---
## BuiltInDocumentProperties.HyperlinksChanged property

Указывает, были ли изменены гиперссылки в документе.

```csharp
public bool HyperlinksChanged { get; }
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
