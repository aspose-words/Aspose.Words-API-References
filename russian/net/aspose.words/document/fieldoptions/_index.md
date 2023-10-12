---
title: Document.FieldOptions
second_title: Справочник по API Aspose.Words для .NET
description: Document свойство. ПолучаетFieldOptions объект который представляет параметры управления обработкой полей в документе.
type: docs
weight: 120
url: /ru/net/aspose.words/document/fieldoptions/
---
## Document.FieldOptions property

Получает[`FieldOptions`](../../../aspose.words.fields/fieldoptions/) объект, который представляет параметры управления обработкой полей в документе.

```csharp
public FieldOptions FieldOptions { get; }
```

### Примеры

Показывает, как указать источник языка и региональных параметров, используемый для форматирования даты во время обновления поля или слияния почты.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем два поля слияния с немецкой локалью.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Установите текущую культуру на английский (США) после сохранения исходного значения в переменной.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Это слияние будет использовать культуру текущего потока для форматирования даты (американский английский).
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Настройте следующее слияние для получения значения культуры из кода поля. Ценность этой культуры будет немецкой.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// Первый результат слияния содержит дату, отформатированную на английском языке, а второй — на немецком.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Восстанавливаем исходную культуру потока.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Смотрите также

* class [FieldOptions](../../../aspose.words.fields/fieldoptions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


