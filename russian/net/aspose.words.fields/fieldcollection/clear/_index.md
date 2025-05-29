---
title: FieldCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words для .NET
description: Легко очистите все поля из FieldCollection с помощью нашего метода Clear. Оптимизируйте управление документами и повысьте эффективность уже сегодня!
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldcollection/clear/
---
## FieldCollection.Clear method

Удаляет все поля этой коллекции из документа и из самой этой коллекции.

```csharp
public void Clear()
```

## Примеры

Показывает, как удалять поля из коллекции полей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder.InsertField(" TIME ");
builder.InsertField(" REVNUM ");
builder.InsertField(" AUTHOR  \"John Doe\" ");
builder.InsertField(" SUBJECT \"My Subject\" ");
builder.InsertField(" QUOTE \"Hello world!\" ");
doc.UpdateFields();

FieldCollection fields = doc.Range.Fields;

Assert.AreEqual(6, fields.Count);

// Ниже приведены четыре способа удаления полей из коллекции полей.
// 1 - Получить поле для удаления:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Получаем коллекцию для удаления поля, которое передаем ее методу удаления:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - Удалить поле из коллекции по индексу:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - Удалить все поля из коллекции сразу:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

### Смотрите также

* class [FieldCollection](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
