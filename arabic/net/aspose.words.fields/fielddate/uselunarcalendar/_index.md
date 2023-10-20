---
title: FieldDate.UseLunarCalendar
linktitle: UseLunarCalendar
articleTitle: UseLunarCalendar
second_title: Aspose.Words لـ .NET
description: FieldDate UseLunarCalendar ملكية. الحصول على أو تحديد ما إذا كان سيتم استخدام التقويم القمري الهجري أو القمري العبري في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fielddate/uselunarcalendar/
---
## FieldDate.UseLunarCalendar property

الحصول على أو تحديد ما إذا كان سيتم استخدام التقويم القمري الهجري أو القمري العبري.

```csharp
public bool UseLunarCalendar { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقول التاريخ لعرض التواريخ وفقًا لأنواع مختلفة من التقويمات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا أردنا أن يعرض النص الموجود في المستند دائمًا التاريخ الصحيح، فيمكننا استخدام حقل التاريخ.
// فيما يلي ثلاثة أنواع من التقويمات الثقافية التي يمكن لحقل التاريخ استخدامها لعرض التاريخ.
// 1 - التقويم القمري الإسلامي:
FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLunarCalendar = true;
Assert.AreEqual(" DATE  \\h", field.GetFieldCode());
builder.Writeln();

// 2 - تقويم أم القرى :
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseUmAlQuraCalendar = true;
Assert.AreEqual(" DATE  \\u", field.GetFieldCode());
builder.Writeln();

// 3 - التقويم الوطني الهندي:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseSakaEraCalendar = true;
Assert.AreEqual(" DATE  \\s", field.GetFieldCode());
builder.Writeln();

// أدخل حقل التاريخ وقم بتعيين نوع التقويم الخاص به على النوع الذي استخدمه التطبيق المضيف آخر مرة.
// في Microsoft Word، سيكون النوع هو الأحدث استخدامًا في الإدراج -> نص -> مربع حوار التاريخ والوقت.
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### أنظر أيضا

* class [FieldDate](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
