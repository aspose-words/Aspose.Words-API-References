---
title: FieldFormat Class
linktitle: FieldFormat
articleTitle: FieldFormat
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.FieldFormat для легкого доступа к числовым, датным и временным полям. Улучшите форматирование документов с помощью мощных функций!
type: docs
weight: 2350
url: /ru/net/aspose.words.fields/fieldformat/
---
## FieldFormat class

Предоставляет типизированный доступ к числовым данным поля, дате и времени, а также общему форматированию.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class FieldFormat
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [DateTimeFormat](../../aspose.words.fields/fieldformat/datetimeformat/) { get; set; } | Возвращает или задает форматирование, применяемое к результату поля даты и времени. Соответствует переключателю \@. |
| [GeneralFormats](../../aspose.words.fields/fieldformat/generalformats/) { get; } | Получает коллекцию общих форматов, которые применяются к числовому, текстовому или любому результату поля. Соответствует переключателям \*. |
| [NumericFormat](../../aspose.words.fields/fieldformat/numericformat/) { get; set; } | Возвращает или задает форматирование, применяемое к результату числового поля. Соответствует переключателю \#. |

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

* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
