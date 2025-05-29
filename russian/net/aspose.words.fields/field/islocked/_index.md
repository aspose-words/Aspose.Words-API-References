---
title: Field.IsLocked
linktitle: IsLocked
articleTitle: IsLocked
second_title: Aspose.Words для .NET
description: Откройте для себя свойство IsLocked для полей — контролируйте пересчет и повышайте целостность данных. Откройте для себя эффективное управление результатами ваших данных сегодня!
type: docs
weight: 50
url: /ru/net/aspose.words.fields/field/islocked/
---
## Field.IsLocked property

Возвращает или задает, заблокировано ли поле (не следует пересчитывать его результат).

```csharp
public bool IsLocked { get; set; }
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

* class [Field](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
