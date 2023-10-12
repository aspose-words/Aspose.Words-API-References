---
title: Enum FieldUpdateCultureSource
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Fields.FieldUpdateCultureSource перечисление. Указывает какую культуру использовать во время обновления поля.
type: docs
weight: 2560
url: /ru/net/aspose.words.fields/fieldupdateculturesource/
---
## FieldUpdateCultureSource enumeration

Указывает, какую культуру использовать во время обновления поля.

```csharp
public enum FieldUpdateCultureSource
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| CurrentThread | `0` | Язык и региональные параметры текущего потока выполнения используются для обновления полей. |
| FieldCode | `1` | Используется культура, указанная в свойствах форматирования поля с помощью настройки языка. |

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

* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)


