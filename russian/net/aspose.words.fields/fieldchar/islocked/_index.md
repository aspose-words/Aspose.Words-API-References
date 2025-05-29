---
title: FieldChar.IsLocked
linktitle: IsLocked
articleTitle: IsLocked
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldChar IsLocked, легко управляйте пересчетом полей. Повысьте точность и эффективность вашего документа сегодня!
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldchar/islocked/
---
## FieldChar.IsLocked property

Возвращает или задает, заблокировано ли родительское поле (не следует пересчитывать его результат).

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

* class [FieldChar](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
