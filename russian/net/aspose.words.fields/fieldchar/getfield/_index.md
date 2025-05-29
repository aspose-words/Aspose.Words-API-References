---
title: FieldChar.GetField
linktitle: GetField
articleTitle: GetField
second_title: Aspose.Words для .NET
description: Откройте для себя метод GetField в FieldChar, легко извлекайте поля для оптимального управления данными и повышения производительности ваших приложений.
type: docs
weight: 40
url: /ru/net/aspose.words.fields/fieldchar/getfield/
---
## FieldChar.GetField method

Возвращает поле для поля char.

```csharp
public Field GetField()
```

### Возвращаемое значение

Поле для полевого символа.

## Примечания

Новый[`Field`](../../field/) объект создается каждый раз при вызове метода.

## Примеры

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

// Извлекаем объект фасада, представляющий поле в документе.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Обновите поле, чтобы отобразить текущую дату.
field.Update();
```

### Смотрите также

* class [Field](../../field/)
* class [FieldChar](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
