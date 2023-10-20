---
title: FieldChar.IsLocked
linktitle: IsLocked
articleTitle: IsLocked
second_title: Aspose.Words для .NET
description: FieldChar IsLocked свойство. Получает или задает заблокировано ли родительское поле не следует пересчитывать его результат на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldchar/islocked/
---
## FieldChar.IsLocked property

Получает или задает, заблокировано ли родительское поле (не следует пересчитывать его результат).

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

// Получаем фасадный объект, который представляет поле в документе.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Обновляем поле, чтобы оно отображало текущую дату.
field.Update();
```

### Смотрите также

* class [FieldChar](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
