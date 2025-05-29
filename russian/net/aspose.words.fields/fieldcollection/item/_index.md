---
title: FieldCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldCollection Item, легко получайте доступ к полям по индексу и повышайте удобство и точность управления данными.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldcollection/item/
---
## FieldCollection indexer

Возвращает поле по указанному индексу.

```csharp
public Field this[int index] { get; }
```

| Параметр | Описание |
| --- | --- |
| index | Указатель коллекции. |

## Примечания

Индекс отсчитывается от нуля.

Отрицательные индексы разрешены и указывают на доступ с конца коллекции. Например, -1 означает последний элемент, -2 означает предпоследний и т. д.

Если индекс больше или равен количеству элементов в списке, возвращается пустая ссылка.

Если индекс отрицательный и его абсолютное значение больше количества элементов в списке, возвращается пустая ссылка.

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

* class [Field](../../field/)
* class [FieldCollection](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
