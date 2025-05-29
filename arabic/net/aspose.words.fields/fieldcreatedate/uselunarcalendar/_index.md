---
title: FieldCreateDate.UseLunarCalendar
linktitle: UseLunarCalendar
articleTitle: UseLunarCalendar
second_title: Aspose.Words لـ .NET
description: أدر تنسيقات التاريخ بسهولة باستخدام خاصية FieldCreateDate UseLunarCalendar. اختر بين التقويمين الهجري والعبري القمري لجدولة دقيقة.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldcreatedate/uselunarcalendar/
---
## FieldCreateDate.UseLunarCalendar property

يحصل على أو يعين ما إذا كان سيتم استخدام التقويم الهجري القمري أو التقويم العبري القمري.

```csharp
public bool UseLunarCalendar { get; set; }
```

## أمثلة

يوضح كيفية استخدام الحقل CREATEDATE لعرض تاريخ/وقت إنشاء المستند.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was created:");

//يمكننا استخدام الحقل CREATEDATE لعرض تاريخ ووقت إنشاء المستند.
// فيما يلي ثلاثة أنواع مختلفة من التقويم والتي وفقًا لها يمكن لحقل CREATEDATE عرض التاريخ/الوقت.
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
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
