---
title: FieldPrintDate.UseUmAlQuraCalendar
linktitle: UseUmAlQuraCalendar
articleTitle: UseUmAlQuraCalendar
second_title: Aspose.Words для .NET
description: Управляйте своими датами без усилий с помощью функции UseUmAlQuraCalendar от FieldPrintDate. Легко переключайте календарь UmalQura для бесперебойной обработки дат.
type: docs
weight: 40
url: /ru/net/aspose.words.fields/fieldprintdate/useumalquracalendar/
---
## FieldPrintDate.UseUmAlQuraCalendar property

Возвращает или задает, использовать ли календарь Ум-аль-Кура.

```csharp
public bool UseUmAlQuraCalendar { get; set; }
```

## Примеры

Показывает прочитанные поля PRINTDATE.

```csharp
Document doc = new Document(MyDir + "Field sample - PRINTDATE.docx");

// Когда документ распечатывается на принтере или распечатывается как PDF (но не экспортируется в PDF),
// Поля PRINTDATE будут отображать дату/время операции печати.
// Если печать не производилась, в этих полях будет отображаться «0/0/0000».
FieldPrintDate field = (FieldPrintDate)doc.Range.Fields[0];

Assert.AreEqual("3/25/2020 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE ", field.GetFieldCode());

// Ниже приведены три различных типа календаря, в соответствии с которыми поле PRINTDATE
// может отображать дату и время последней операции печати.
// 1 - Исламский лунный календарь:
field = (FieldPrintDate)doc.Range.Fields[1];

Assert.True(field.UseLunarCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\h", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[2];

// 2 - Календарь Умм аль-Кура:
Assert.True(field.UseUmAlQuraCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\u", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[3];

// 3 - Индийский национальный календарь:
Assert.True(field.UseSakaEraCalendar);
Assert.AreEqual("1/5/1942 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\s", field.GetFieldCode());
```

### Смотрите также

* class [FieldPrintDate](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
