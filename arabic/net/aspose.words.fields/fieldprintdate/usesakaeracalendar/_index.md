---
title: FieldPrintDate.UseSakaEraCalendar
linktitle: UseSakaEraCalendar
articleTitle: UseSakaEraCalendar
second_title: Aspose.Words لـ .NET
description: FieldPrintDate UseSakaEraCalendar ملكية. الحصول على أو تعيين ما إذا كان سيتم استخدام تقويم Saka Era في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldprintdate/usesakaeracalendar/
---
## FieldPrintDate.UseSakaEraCalendar property

الحصول على أو تعيين ما إذا كان سيتم استخدام تقويم Saka Era.

```csharp
public bool UseSakaEraCalendar { get; set; }
```

## أمثلة

يظهر قراءة حقول PRINTDATE.

```csharp
Document doc = new Document(MyDir + "Field sample - PRINTDATE.docx");

// عندما تتم طباعة مستند بواسطة الطابعة أو طباعته كملف PDF (ولكن لا يتم تصديره إلى PDF)،
// ستعرض حقول PRINTDATE تاريخ/وقت عملية الطباعة.
// إذا لم تتم الطباعة، فستعرض هذه الحقول "0/0/0000".
FieldPrintDate field = (FieldPrintDate)doc.Range.Fields[0];

Assert.AreEqual("3/25/2020 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE ", field.GetFieldCode());

// فيما يلي ثلاثة أنواع تقويم مختلفة يتم وفقًا لها حقل PRINTDATE
// يمكنه عرض تاريخ ووقت آخر عملية طباعة.
// 1 - التقويم القمري الإسلامي:
field = (FieldPrintDate)doc.Range.Fields[1];

Assert.True(field.UseLunarCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\h", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[2];

// 2 - تقويم أم القرى :
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
