---
title: BuiltInDocumentProperties.ScaleCrop
linktitle: ScaleCrop
articleTitle: ScaleCrop
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ScaleCrop в BuiltInDocumentProperties, которое управляет отображением миниатюр, обеспечивая оптимальный просмотр обрезанных или масштабированных изображений.
type: docs
weight: 260
url: /ru/net/aspose.words.properties/builtindocumentproperties/scalecrop/
---
## BuiltInDocumentProperties.ScaleCrop property

Указывает, обрезается ли миниатюра документа или масштабируется для соответствия размеру дисплея.

```csharp
public bool ScaleCrop { get; }
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
