---
title: FieldChar.IsDirty
linktitle: IsDirty
articleTitle: IsDirty
second_title: Aspose.Words для .NET
description: Узнайте, как свойство FieldChar IsDirty помогает поддерживать точность документа, отслеживая изменения и гарантируя, что ваши поля всегда отражают последние обновления.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldchar/isdirty/
---
## FieldChar.IsDirty property

Возвращает или задает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений , внесенных в документ.

```csharp
public bool IsDirty { get; set; }
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
