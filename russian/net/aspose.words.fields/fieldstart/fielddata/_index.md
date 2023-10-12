---
title: FieldStart.FieldData
second_title: Справочник по API Aspose.Words для .NET
description: FieldStart свойство. Получает данные настраиваемого поля связанные с полем.
type: docs
weight: 10
url: /ru/net/aspose.words.fields/fieldstart/fielddata/
---
## FieldStart.FieldData property

Получает данные настраиваемого поля, связанные с полем.

```csharp
public byte[] FieldData { get; }
```

### Примеры

Показывает, как получить данные, связанные с полем.

```csharp
Document doc = new Document(MyDir + "Field sample - Field with data.docx");

Field field = doc.Range.Fields[2];
Console.WriteLine(Encoding.Default.GetString(field.Start.FieldData));
```

### Смотрите также

* class [FieldStart](../)
* пространство имен [Aspose.Words.Fields](../../fieldstart/)
* сборка [Aspose.Words](../../../)


