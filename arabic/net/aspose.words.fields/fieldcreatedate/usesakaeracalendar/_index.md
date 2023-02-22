---
title: FieldCreateDate.UseSakaEraCalendar
second_title: Aspose.Words لمراجع .NET API
description: FieldCreateDate ملكية. يحصل أو يحدد ما إذا كان سيتم استخدام تقويم Saka Era .
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldcreatedate/usesakaeracalendar/
---
## FieldCreateDate.UseSakaEraCalendar property

يحصل أو يحدد ما إذا كان سيتم استخدام تقويم Saka Era .

```csharp
public bool UseSakaEraCalendar { get; set; }
```

### أمثلة

يوضح كيفية استخدام حقل الإنشاء لعرض تاريخ / وقت إنشاء المستند.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was created:");

// يمكننا استخدام حقل الإنشاء لعرض تاريخ ووقت إنشاء المستند.
// فيما يلي ثلاثة أنواع مختلفة من التقويمات التي يمكن أن يعرض حقل الإنشاء التاريخ / الوقت وفقًا لها.
// 1 - التقويم القمري الإسلامي:
builder.Write("According to the Lunar Calendar - ");
FieldCreateDate field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" CREATEDATE  \\h", field.GetFieldCode());

// 2 - تقويم أم القرى:
builder.Write("\nAccording to the Umm al-Qura Calendar - ");
field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" CREATEDATE  \\u", field.GetFieldCode());

// 3 - التقويم الوطني الهندي:
builder.Write("\nAccording to the Indian National Calendar - ");
field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" CREATEDATE  \\s", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CREATEDATE.docx");
```

### أنظر أيضا

* class [FieldCreateDate](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldcreatedate/)
* المجسم [Aspose.Words](../../../)


