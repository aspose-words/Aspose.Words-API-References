---
title: FieldCreateDate.UseUmAlQuraCalendar
linktitle: UseUmAlQuraCalendar
articleTitle: UseUmAlQuraCalendar
second_title: Aspose.Words для .NET
description: FieldCreateDate UseUmAlQuraCalendar свойство. Получает или задает необходимость использования календаря УмальКура на С#.
type: docs
weight: 40
url: /ru/net/aspose.words.fields/fieldcreatedate/useumalquracalendar/
---
## FieldCreateDate.UseUmAlQuraCalendar property

Получает или задает необходимость использования календаря Ум-аль-Кура.

```csharp
public bool UseUmAlQuraCalendar { get; set; }
```

## Примеры

Показывает, как использовать поле CREATEDATE для отображения даты/времени создания документа.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was created:");

// Мы можем использовать поле CREATEDATE для отображения даты и времени создания документа.
// Ниже приведены три различных типа календаря, в соответствии с которыми поле CREATEDATE может отображать дату/время.
// 1 - Исламский лунный календарь:
builder.Write("According to the Lunar Calendar - ");
FieldCreateDate field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" CREATEDATE  \\h", field.GetFieldCode());

// 2 - Календарь Умм аль-Кура:
builder.Write("\nAccording to the Umm al-Qura Calendar - ");
field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" CREATEDATE  \\u", field.GetFieldCode());

// 3 - Индийский национальный календарь:
builder.Write("\nAccording to the Indian National Calendar - ");
field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" CREATEDATE  \\s", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CREATEDATE.docx");
```

### Смотрите также

* class [FieldCreateDate](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
