---
title: Field.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words для .NET
description: Field Type свойство. Получает тип поля Microsoft Word на С#.
type: docs
weight: 100
url: /ru/net/aspose.words.fields/field/type/
---
## Field.Type property

Получает тип поля Microsoft Word.

```csharp
public virtual FieldType Type { get; }
```

## Примеры

Показывает, как вставить поле в документ с помощью кода поля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Эта перегрузка метода InsertField автоматически обновляет вставленные поля.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

### Смотрите также

* enum [FieldType](../../fieldtype/)
* class [Field](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
