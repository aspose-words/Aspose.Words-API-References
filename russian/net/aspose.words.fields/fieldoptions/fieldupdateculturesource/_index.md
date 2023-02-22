---
title: FieldOptions.FieldUpdateCultureSource
second_title: Справочник по API Aspose.Words для .NET
description: FieldOptions свойство. Указывает какую культуру использовать для форматирования результата поля.
type: docs
weight: 100
url: /ru/net/aspose.words.fields/fieldoptions/fieldupdateculturesource/
---
## FieldOptions.FieldUpdateCultureSource property

Указывает, какую культуру использовать для форматирования результата поля.

```csharp
public FieldUpdateCultureSource FieldUpdateCultureSource { get; set; }
```

### Примечания

По умолчанию используется культура текущего потока.

Настройка влияет только на поля даты/времени с переключателем формата \\@.

### Примеры

Показывает, как указать источник языка и региональных параметров, используемых для форматирования даты во время обновления поля или слияния.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем два поля слияния с немецкой локалью.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Установите текущую культуру на американский английский после сохранения исходного значения в переменной.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Это слияние будет использовать язык и региональные параметры текущего потока для форматирования даты, американский английский.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Настройте следующее слияние, чтобы получить значение культуры из кода поля. Ценность этой культуры будет немецкой.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// Первый результат слияния содержит дату в английском формате, а второй — в немецком.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Восстановить исходную культуру потока.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Смотрите также

* enum [FieldUpdateCultureSource](../../fieldupdateculturesource/)
* class [FieldOptions](../)
* пространство имен [Aspose.Words.Fields](../../fieldoptions/)
* сборка [Aspose.Words](../../../)


