---
title: FieldPrintDate.UseLunarCalendar
linktitle: UseLunarCalendar
articleTitle: UseLunarCalendar
second_title: Aspose.Words لـ .NET
description: أدر التواريخ بسهولة باستخدام خاصية FieldPrintDate UseLunarCalendar. يمكنك التبديل بسهولة بين التقويمين الهجري والعبري القمري لضمان تكامل سلس.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldprintdate/uselunarcalendar/
---
## FieldPrintDate.UseLunarCalendar property

يحصل على أو يعين ما إذا كان سيتم استخدام التقويم الهجري القمري أو التقويم العبري القمري.

```csharp
public bool UseLunarCalendar { get; set; }
```

## أمثلة

يعرض حقول PRINTDATE المقروءة.

```csharp
Document doc = new Document(MyDir + "Field sample - PRINTDATE.docx");

// عند طباعة مستند بواسطة طابعة أو طباعته كملف PDF (ولكن لا يتم تصديره إلى PDF)،
// ستعرض حقول PRINTDATE تاريخ/وقت عملية الطباعة.
// إذا لم تتم عملية الطباعة، فسوف تعرض هذه الحقول "0/0/0000".
FieldPrintDate field = (FieldPrintDate)doc.Range.Fields[0];

Assert.AreEqual("3/25/2020 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE ", field.GetFieldCode());

// فيما يلي ثلاثة أنواع مختلفة من التقويم والتي وفقًا لها يتم تحديد حقل PRINTDATE
//يمكن عرض التاريخ والوقت لآخر عملية طباعة.
// 1 - التقويم القمري الإسلامي:
field = (FieldPrintDate)doc.Range.Fields[1];

Assert.True(field.UseLunarCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\h", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[2];

// 2 - تقويم أم القرى:
Assert.True(field.UseUmAlQuraCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\u", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[3];

// 3 - التقويم الوطني الهندي:
Assert.True(field.UseSakaEraCalendar);
Assert.AreEqual("1/5/1942 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\s", field.GetFieldCode());
```

### أنظر أيضا

* class [FieldPrintDate](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
