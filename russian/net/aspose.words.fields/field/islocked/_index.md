---
title: Field.IsLocked
second_title: Справочник по API Aspose.Words для .NET
description: Field свойство. Получает или задает заблокировано ли поле не следует пересчитывать результат.
type: docs
weight: 50
url: /ru/net/aspose.words.fields/field/islocked/
---
## Field.IsLocked property

Получает или задает, заблокировано ли поле (не следует пересчитывать результат).

```csharp
public bool IsLocked { get; set; }
```

### Примеры

Показывает, как работать с узлом FieldStart.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.Format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

FieldChar fieldStart = field.Start;

Assert.AreEqual(FieldType.FieldDate, fieldStart.FieldType);
Assert.AreEqual(false, fieldStart.IsDirty);
Assert.AreEqual(false, fieldStart.IsLocked);

// Получаем фасадный объект, который представляет поле в документе.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Обновляем поле, чтобы оно отображало текущую дату.
field.Update();
```

### Смотрите также

* class [Field](../)
* пространство имен [Aspose.Words.Fields](../../field/)
* сборка [Aspose.Words](../../../)


