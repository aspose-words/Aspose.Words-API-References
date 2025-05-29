---
title: FieldStart.FieldData
linktitle: FieldData
articleTitle: FieldData
second_title: Aspose.Words для .NET
description: Разблокируйте пользовательские полевые данные с помощью свойства FieldData в FieldStart, улучшив управление данными и повысив производительность без особых усилий.
type: docs
weight: 10
url: /ru/net/aspose.words.fields/fieldstart/fielddata/
---
## FieldStart.FieldData property

Получает данные пользовательского поля, связанные с полем.

```csharp
public byte[] FieldData { get; }
```

## Примеры

Показывает, как получить данные, связанные с полем.

```csharp
Document doc = new Document(MyDir + "Field sample - Field with data.docx");

Field field = doc.Range.Fields[2];
Console.WriteLine(Encoding.UTF8.GetString(field.Start.FieldData));
```

### Смотрите также

* class [FieldStart](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
