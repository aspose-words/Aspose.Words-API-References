---
title: GeneralFormatCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: Воспользуйтесь свойством GeneralFormatCollection Item, чтобы легко получить настраиваемые форматы по любому индексу, что позволит без труда улучшить представление данных.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/generalformatcollection/item/
---
## GeneralFormatCollection indexer

Получает общий формат по указанному индексу.

```csharp
public GeneralFormat this[int index] { get; }
```

| Параметр | Описание |
| --- | --- |
| index | Индекс общего формата. |

### Возвращаемое значение

Общий формат.

## Примеры

Показывает, как форматировать результаты полей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Используйте конструктор документов, чтобы вставить поле, отображающее результат без применения форматирования.
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

// Мы можем применить формат к результату поля, используя свойства поля.
// Ниже приведены три типа форматов, которые мы можем применить к результату поля.
// 1 - Числовой формат:
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.AreEqual("= 2 + 3 \\# $###.00", field.GetFieldCode());
Assert.AreEqual("$  5.00", field.Result);

// 2 - Формат даты/времени:
field = builder.InsertField("DATE");
format = field.Format;
format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());
Console.WriteLine($"Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

// 3 - Общий формат:
field = builder.InsertField("= 25 + 33");
format = field.Format;
format.GeneralFormats.Add(GeneralFormat.LowercaseRoman);
format.GeneralFormats.Add(GeneralFormat.Upper);
field.Update();

int index = 0;
using (IEnumerator<GeneralFormat> generalFormatEnumerator = format.GeneralFormats.GetEnumerator())
    while (generalFormatEnumerator.MoveNext())
        Console.WriteLine($"General format index {index++}: {generalFormatEnumerator.Current}");

Assert.AreEqual("= 25 + 33 \\* roman \\* Upper", field.GetFieldCode());
Assert.AreEqual("LVIII", field.Result);
Assert.AreEqual(2, format.GeneralFormats.Count);
Assert.AreEqual(GeneralFormat.LowercaseRoman, format.GeneralFormats[0]);

// Мы можем удалить наши форматы, чтобы вернуть результат поля к исходному виду.
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### Смотрите также

* enum [GeneralFormat](../../generalformat/)
* class [GeneralFormatCollection](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
