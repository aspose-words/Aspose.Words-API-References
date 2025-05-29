---
title: FileFormatInfo.HasMacros
linktitle: HasMacros
articleTitle: HasMacros
second_title: Aspose.Words для .NET
description: Узнайте, содержит ли ваш документ макросы VBA с помощью свойства FileFormatInfo HasMacros. Обеспечьте безопасность и функциональность документа сегодня!
type: docs
weight: 30
url: /ru/net/aspose.words/fileformatinfo/hasmacros/
---
## FileFormatInfo.HasMacros property

Возврат`истинный` если этот документ содержит макросы VBA.

```csharp
public bool HasMacros { get; }
```

## Примеры

Показывает, как проверить наличие макроса VBA без загрузки документа.

```csharp
FileFormatInfo fileFormatInfo = FileFormatUtil.DetectFileFormat(MyDir + "Macro.docm");
Assert.IsTrue(fileFormatInfo.HasMacros);
```

### Смотрите также

* class [FileFormatInfo](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
