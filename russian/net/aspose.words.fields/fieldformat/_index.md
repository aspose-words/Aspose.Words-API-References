---
title: FieldFormat
second_title: Справочник по API Aspose.Words для .NET
description: Предоставляет типизированный доступ к числовым значениям поля дате и времени а также к общему форматированию.
type: docs
weight: 1790
url: /ru/net/aspose.words.fields/fieldformat/
---
## FieldFormat class

Предоставляет типизированный доступ к числовым значениям поля, дате и времени, а также к общему форматированию.

```csharp
public class FieldFormat
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [DateTimeFormat](../../aspose.words.fields/fieldformat/datetimeformat) { get; set; } | Получает или задает форматирование, которое применяется к результату поля даты и времени. Соответствует переключателю \@. |
| [GeneralFormats](../../aspose.words.fields/fieldformat/generalformats) { get; } | Получает набор общих форматов, которые применяются к числовому, текстовому или любому результату поля. Соответствует переключателям \*. |
| [NumericFormat](../../aspose.words.fields/fieldformat/numericformat) { get; set; } | Получает или задает форматирование, которое применяется к результату числового поля. Соответствует переключателю \#. |

### Примеры

Показывает, как форматировать результаты поля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Используйте конструктор документов, чтобы вставить поле, отображающее результат без применения формата.
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

// Мы можем удалить наши форматы, чтобы вернуть результат поля в исходную форму.
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### Смотрите также

* пространство имен [Aspose.Words.Fields](../../aspose.words.fields)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->