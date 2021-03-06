---
title: LocaleId
second_title: Справочник по API Aspose.Words для .NET
description: Получает или задает LCID поля.
type: docs
weight: 60
url: /ru/net/aspose.words.fields/field/localeid/
---
## Field.LocaleId property

Получает или задает LCID поля.

```csharp
public int LocaleId { get; set; }
```

### Примеры

Показывает, как вставить поле и работать с его локалью.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте поле DATE, а затем напечатайте дату, которую оно будет отображать.
// Текущая культура вашего потока определяет формат даты.
Field field = builder.InsertField(@"DATE");
Console.WriteLine($"Today's date, as displayed in the \"{CultureInfo.CurrentCulture.EnglishName}\" culture: {field.Result}");

Assert.AreEqual(1033, field.LocaleId);
// Изменение культуры нашего потока повлияет на результат поля DATE.
// Другой способ заставить поле DATE отображать дату в другом языке и региональных параметрах — использовать его свойство LocaleId.
// Этот способ позволяет нам избежать изменения культуры потока, чтобы получить этот эффект.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
CultureInfo de = new CultureInfo("de-DE");
field.LocaleId = de.LCID;
field.Update();

Console.WriteLine($"Today's date, as displayed according to the \"{CultureInfo.GetCultureInfo(field.LocaleId).EnglishName}\" culture: {field.Result}");
```

### Смотрите также

* class [Field](../../field)
* пространство имен [Aspose.Words.Fields](../../field)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
