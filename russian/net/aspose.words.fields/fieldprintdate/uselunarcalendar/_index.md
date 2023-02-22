---
title: FieldPrintDate.UseLunarCalendar
second_title: Справочник по API Aspose.Words для .NET
description: FieldPrintDate свойство. Получает или задает использование лунного календаря по хиджре или лунного календаря на иврите.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldprintdate/uselunarcalendar/
---
## FieldPrintDate.UseLunarCalendar property

Получает или задает использование лунного календаря по хиджре или лунного календаря на иврите.

```csharp
public bool UseLunarCalendar { get; set; }
```

### Примеры

Показывает прочитанные поля PRINTDATE.

```csharp
Document doc = new Document(MyDir + "Field sample - PRINTDATE.docx");

// Когда документ распечатывается на принтере или распечатывается в формате PDF (но не экспортируется в PDF),
// Поля PRINTDATE будут отображать дату/время операции печати.
// Если печать не производилась, в этих полях будет отображаться "0/0/0000".
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
* пространство имен [Aspose.Words.Fields](../../fieldprintdate/)
* сборка [Aspose.Words](../../../)


