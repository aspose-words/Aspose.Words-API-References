---
title: Field.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: Aspose.Words для .NET
description: Field LocaleId свойство. Получает или задает LCID поля на С#.
type: docs
weight: 60
url: /ru/net/aspose.words.fields/field/localeid/
---
## Field.LocaleId property

Получает или задает LCID поля.

```csharp
public int LocaleId { get; set; }
```

## Примеры

Показывает, как вставить поле и работать с его языковым стандартом.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем поле ДАТА, а затем печатаем дату, которую оно будет отображать.
// Текущая культура вашего потока определяет формат даты.
Field field = builder.InsertField(@"DATE");
Console.WriteLine($"Today's date, as displayed in the \"{CultureInfo.CurrentCulture.EnglishName}\" culture: {field.Result}");

Assert.AreEqual(1033, field.LocaleId);
// Изменение культуры нашего потока повлияет на результат поля DATE.
// Другой способ заставить поле ДАТА отображать дату в другой культуре — использовать его свойство LocaleId.
// Этот способ позволяет нам избежать изменения культуры потока для достижения такого эффекта.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
CultureInfo de = new CultureInfo("de-DE");
field.LocaleId = de.LCID;
field.Update();

Console.WriteLine($"Today's date, as displayed according to the \"{CultureInfo.GetCultureInfo(field.LocaleId).EnglishName}\" culture: {field.Result}");
```

### Смотрите также

* class [Field](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
