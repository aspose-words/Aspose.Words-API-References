---
title: FieldDate.UseLastFormat
linktitle: UseLastFormat
articleTitle: UseLastFormat
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية FieldDate UseLastFormat على تعزيز سير عملك من خلال الاحتفاظ بتنسيق التاريخ المستخدم الأخير لتحقيق التكامل السلس في تطبيقاتك.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fielddate/uselastformat/
---
## FieldDate.UseLastFormat property

يحصل على أو يحدد ما إذا كان سيتم استخدام التنسيق الذي استخدمه تطبيق الاستضافة آخر مرة عند إدراج حقل DATE جديد.

```csharp
public bool UseLastFormat { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقول التاريخ لعرض التواريخ وفقًا لأنواع مختلفة من التقويمات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا أردنا أن يعرض النص الموجود في المستند التاريخ الصحيح دائمًا، فيمكننا استخدام حقل DATE.
// فيما يلي ثلاثة أنواع من التقويمات الثقافية التي يمكن لحقل DATE استخدامها لعرض التاريخ.
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

// أدخل حقل DATE وقم بتعيين نوع التقويم الخاص به إلى النوع الأخير الذي يستخدمه تطبيق المضيف.
// في Microsoft Word، سيكون النوع هو الأحدث استخدامًا في مربع الحوار إدراج -> نص -> التاريخ والوقت.
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
