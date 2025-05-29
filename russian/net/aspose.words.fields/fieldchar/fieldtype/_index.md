---
title: FieldChar.FieldType
linktitle: FieldType
articleTitle: FieldType
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldChar FieldType, которое раскрывает тип поля, улучшая управление данными и эффективность программирования. Узнайте больше прямо сейчас!
type: docs
weight: 10
url: /ru/net/aspose.words.fields/fieldchar/fieldtype/
---
## FieldChar.FieldType property

Возвращает тип поля.

```csharp
public FieldType FieldType { get; }
```

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

* enum [FieldType](../../fieldtype/)
* class [FieldChar](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
