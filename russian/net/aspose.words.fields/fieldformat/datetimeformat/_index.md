---
title: FieldFormat.DateTimeFormat
second_title: Справочник по API Aspose.Words для .NET
description: FieldFormat свойство. Получает или задает форматирование которое применяется к результату поля даты и времени. Соответствует переключателю .
type: docs
weight: 10
url: /ru/net/aspose.words.fields/fieldformat/datetimeformat/
---
## FieldFormat.DateTimeFormat property

Получает или задает форматирование, которое применяется к результату поля даты и времени. Соответствует переключателю \@.

```csharp
public string DateTimeFormat { get; set; }
```

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

* class [FieldFormat](../)
* пространство имен [Aspose.Words.Fields](../../fieldformat/)
* сборка [Aspose.Words](../../../)


