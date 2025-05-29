---
title: FieldDate.UseLastFormat
linktitle: UseLastFormat
articleTitle: UseLastFormat
second_title: Aspose.Words для .NET
description: Узнайте, как свойство FieldDate UseLastFormat улучшает ваш рабочий процесс, сохраняя последний использованный формат даты для бесшовной интеграции в ваши приложения.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fielddate/uselastformat/
---
## FieldDate.UseLastFormat property

Возвращает или задает, следует ли использовать последний формат, использованный приложением хостинга при вставке нового поля ДАТА.

```csharp
public bool UseLastFormat { get; set; }
```

## Примеры

Показывает, как использовать поля ДАТА для отображения дат в соответствии с различными видами календарей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Если мы хотим, чтобы текст в документе всегда отображал правильную дату, мы можем использовать поле ДАТА.
// Ниже приведены три типа культурных календарей, которые поле ДАТА может использовать для отображения даты.
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

// Вставьте поле ДАТА и установите его тип календаря на последний, использовавшийся хост-приложением.
// В Microsoft Word тип будет последним использованным в диалоговом окне Вставка -> Текст -> Дата и время.
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### Смотрите также

* class [FieldDate](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
