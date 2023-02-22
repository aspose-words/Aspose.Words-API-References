---
title: FieldDate.UseLunarCalendar
second_title: Aspose.Words لمراجع .NET API
description: FieldDate ملكية. يحصل أو يحدد ما إذا كان سيتم استخدام التقويم الهجري القمري أو التقويم القمري العبري.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fielddate/uselunarcalendar/
---
## FieldDate.UseLunarCalendar property

يحصل أو يحدد ما إذا كان سيتم استخدام التقويم الهجري القمري أو التقويم القمري العبري.

```csharp
public bool UseLunarCalendar { get; set; }
```

### أمثلة

يوضح كيفية استخدام حقول التاريخ لعرض التواريخ وفقًا لأنواع التقويمات المختلفة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا أردنا دائمًا أن يعرض النص الموجود في المستند التاريخ الصحيح ، فيمكننا استخدام حقل التاريخ.
// فيما يلي ثلاثة أنواع من التقاويم الثقافية التي يمكن أن يستخدمها حقل التاريخ لعرض التاريخ.
// 1 - التقويم القمري الإسلامي:
FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLunarCalendar = true;
Assert.AreEqual(" DATE  \\h", field.GetFieldCode());
builder.Writeln();

// 2 - تقويم أم القرى:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseUmAlQuraCalendar = true;
Assert.AreEqual(" DATE  \\u", field.GetFieldCode());
builder.Writeln();

// 3 - التقويم الوطني الهندي:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseSakaEraCalendar = true;
Assert.AreEqual(" DATE  \\s", field.GetFieldCode());
builder.Writeln();

// أدخل حقل التاريخ وقم بتعيين نوع التقويم الخاص به على آخر نوع استخدمه التطبيق المضيف.
// في Microsoft Word ، سيكون النوع هو الأحدث استخدامًا في Insert - > نص - >. مربع حوار التاريخ والوقت.
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### أنظر أيضا

* class [FieldDate](../)
* مساحة الاسم [Aspose.Words.Fields](../../fielddate/)
* المجسم [Aspose.Words](../../../)


