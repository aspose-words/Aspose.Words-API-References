---
title: Field.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: Aspose.Words для .NET
description: Управляйте свойством LocaleId вашего поля без усилий. Получите или установите LCID для улучшенной локализации и пользовательского опыта в ваших приложениях.
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

Показывает, как вставить поле и работать с его локалью.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте поле ДАТА, а затем выведите дату, которая будет отображаться.
// Текущая культура вашего потока определяет формат даты.
Field field = builder.InsertField(@"DATE");
Console.WriteLine($"Today's date, as displayed in the \"{CultureInfo.CurrentCulture.EnglishName}\" culture: {field.Result}");

Assert.AreEqual(1033, field.LocaleId);
// Изменение культуры нашего потока повлияет на результат поля ДАТА.
// Другой способ заставить поле ДАТА отображать дату в другой культуре — использовать его свойство LocaleId.
// Этот способ позволяет нам избежать изменения культуры потока для получения этого эффекта.
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
