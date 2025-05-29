---
title: FieldUpdateCultureSource Enum
linktitle: FieldUpdateCultureSource
articleTitle: FieldUpdateCultureSource
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.Fields.FieldUpdateCultureSource. Управляйте обновлениями полей с помощью настраиваемых параметров языка и региональных параметров для повышения точности документов.
type: docs
weight: 2970
url: /ru/net/aspose.words.fields/fieldupdateculturesource/
---
## FieldUpdateCultureSource enumeration

Указывает, какую культуру использовать при обновлении поля.

```csharp
public enum FieldUpdateCultureSource
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| CurrentThread | `0` | Для обновления полей используется культура текущего потока выполнения. |
| FieldCode | `1` | Используется культура, указанная в свойствах форматирования поля через настройку языка. |

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

* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
