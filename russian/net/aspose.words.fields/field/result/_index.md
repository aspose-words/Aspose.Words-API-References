---
title: Field.Result
linktitle: Result
articleTitle: Result
second_title: Aspose.Words для .NET
description: Field Result свойство. Получает или задает текст расположенный между разделителем полей и концом поля на С#.
type: docs
weight: 70
url: /ru/net/aspose.words.fields/field/result/
---
## Field.Result property

Получает или задает текст, расположенный между разделителем полей и концом поля.

```csharp
public string Result { get; set; }
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

* class [Field](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
