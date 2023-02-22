---
title: FieldDate.UseSakaEraCalendar
second_title: Справочник по API Aspose.Words для .NET
description: FieldDate свойство. Получает или задает следует ли использовать календарь Эры Сака.
type: docs
weight: 40
url: /ru/net/aspose.words.fields/fielddate/usesakaeracalendar/
---
## FieldDate.UseSakaEraCalendar property

Получает или задает, следует ли использовать календарь Эры Сака.

```csharp
public bool UseSakaEraCalendar { get; set; }
```

### Примеры

Показывает, как использовать поля DATE для отображения дат в соответствии с различными типами календарей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Если мы хотим, чтобы текст в документе всегда отображал правильную дату, мы можем использовать поле ДАТА.
// Ниже приведены три типа культурных календарей, которые поле DATE может использовать для отображения даты.
// 1 - Исламский лунный календарь:
FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLunarCalendar = true;
Assert.AreEqual(" DATE  \\h", field.GetFieldCode());
builder.Writeln();

// 2 - Календарь Умм аль-Кура:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseUmAlQuraCalendar = true;
Assert.AreEqual(" DATE  \\u", field.GetFieldCode());
builder.Writeln();

// 3 - Индийский национальный календарь:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseSakaEraCalendar = true;
Assert.AreEqual(" DATE  \\s", field.GetFieldCode());
builder.Writeln();

// Вставьте поле ДАТА и установите его тип календаря на тот, который последний раз использовался хост-приложением.
// В Microsoft Word тип будет самым последним использованным во вставке -> Текст -> Диалоговое окно «Дата и время».
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### Смотрите также

* class [FieldDate](../)
* пространство имен [Aspose.Words.Fields](../../fielddate/)
* сборка [Aspose.Words](../../../)


