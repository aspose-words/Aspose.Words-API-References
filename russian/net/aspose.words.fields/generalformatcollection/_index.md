---
title: GeneralFormatCollection Class
linktitle: GeneralFormatCollection
articleTitle: GeneralFormatCollection
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.GeneralFormatCollection — мощную типизированную коллекцию для легкого управления общими форматами в ваших документах.
type: docs
weight: 3060
url: /ru/net/aspose.words.fields/generalformatcollection/
---
## GeneralFormatCollection class

Представляет типизированную коллекцию общих форматов.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class GeneralFormatCollection : IEnumerable<GeneralFormat>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.fields/generalformatcollection/count/) { get; } | Получает общее количество элементов в коллекции. |
| [Item](../../aspose.words.fields/generalformatcollection/item/) { get; } | Получает общий формат по указанному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words.fields/generalformatcollection/add/)(*[GeneralFormat](../generalformat/)*) | Добавляет общий формат в коллекцию. |
| [GetEnumerator](../../aspose.words.fields/generalformatcollection/getenumerator/)() | Возвращает объект перечислителя. |
| [Remove](../../aspose.words.fields/generalformatcollection/remove/)(*[GeneralFormat](../generalformat/)*) | Удаляет все вхождения указанного общего формата из коллекции. |
| [RemoveAt](../../aspose.words.fields/generalformatcollection/removeat/)(*int*) | Удаляет вхождение общего формата по указанному индексу. |

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

* enum [GeneralFormat](../generalformat/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
