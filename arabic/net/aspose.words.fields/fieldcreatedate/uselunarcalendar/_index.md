---
title: FieldCreateDate.UseLunarCalendar
linktitle: UseLunarCalendar
articleTitle: UseLunarCalendar
second_title: Aspose.Words لـ .NET
description: FieldCreateDate UseLunarCalendar ملكية. الحصول على أو تحديد ما إذا كان سيتم استخدام التقويم القمري الهجري أو القمري العبري في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldcreatedate/uselunarcalendar/
---
## FieldCreateDate.UseLunarCalendar property

الحصول على أو تحديد ما إذا كان سيتم استخدام التقويم القمري الهجري أو القمري العبري.

```csharp
public bool UseLunarCalendar { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقل "تاريخ الإنشاء" لعرض تاريخ/وقت إنشاء المستند.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was created:");

// يمكننا استخدام حقل تاريخ الإنشاء لعرض تاريخ ووقت إنشاء المستند.
// فيما يلي ثلاثة أنواع تقويم مختلفة يمكن لحقل "التاريخ الإنشاء" من خلالها عرض التاريخ/الوقت.
// 1 - التقويم القمري الإسلامي:
builder.Write("According to the Lunar Calendar - ");
FieldCreateDate field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" CREATEDATE  \\h", field.GetFieldCode());

// 2 - تقويم أم القرى :
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
