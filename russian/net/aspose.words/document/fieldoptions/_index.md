---
title: Document.FieldOptions
linktitle: FieldOptions
articleTitle: FieldOptions
second_title: Aspose.Words для .NET
description: Изучите свойство Document FieldOptions для эффективного управления обработкой полей. Откройте для себя уникальные возможности для улучшенного контроля и настройки документов.
type: docs
weight: 130
url: /ru/net/aspose.words/document/fieldoptions/
---
## Document.FieldOptions property

Получает[`FieldOptions`](../../../aspose.words.fields/fieldoptions/) объект, представляющий параметры управления обработкой полей в документе.

```csharp
public FieldOptions FieldOptions { get; }
```

## Примеры

Показывает, как указать источник культуры, используемый для форматирования даты во время обновления полей или слияния почты.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте два поля слияния с немецкой локалью.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Установите текущий язык и региональные параметры на американский английский, сохранив исходное значение в переменной.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Это слияние будет использовать региональные параметры текущего потока для форматирования даты — американский английский.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Настройте следующее слияние для получения значения культуры из кода поля. Значение этой культуры будет немецким.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// Первый результат слияния содержит дату, отформатированную на английском языке, а второй — на немецком.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Восстановить исходную культуру потока.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Смотрите также

* class [FieldOptions](../../../aspose.words.fields/fieldoptions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
