---
title: FieldCreateDate.UseUmAlQuraCalendar
linktitle: UseUmAlQuraCalendar
articleTitle: UseUmAlQuraCalendar
second_title: Aspose.Words لـ .NET
description: FieldCreateDate UseUmAlQuraCalendar ملكية. الحصول على أو تحديد ما إذا كان سيتم استخدام تقويم أم القرى في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.fields/fieldcreatedate/useumalquracalendar/
---
## FieldCreateDate.UseUmAlQuraCalendar property

الحصول على أو تحديد ما إذا كان سيتم استخدام تقويم أم القرى.

```csharp
public bool UseUmAlQuraCalendar { get; set; }
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
