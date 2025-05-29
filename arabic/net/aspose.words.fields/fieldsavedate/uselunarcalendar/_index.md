---
title: FieldSaveDate.UseLunarCalendar
linktitle: UseLunarCalendar
articleTitle: UseLunarCalendar
second_title: Aspose.Words لـ .NET
description: تتيح لك خاصية UseLunarCalendar في FieldSaveDate التبديل بسهولة بين التقويمات القمرية الهجرية والعبرية لإدارة التاريخ بسلاسة.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldsavedate/uselunarcalendar/
---
## FieldSaveDate.UseLunarCalendar property

يحصل على أو يعين ما إذا كان سيتم استخدام التقويم الهجري القمري أو التقويم العبري القمري.

```csharp
public bool UseLunarCalendar { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقل SAVEDATE لعرض تاريخ/وقت عملية حفظ المستند الأحدث التي تم إجراؤها باستخدام Microsoft Word.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was last saved:");

// يمكننا استخدام حقل SAVEDATE لعرض تاريخ ووقت آخر عملية حفظ للمستند.
// عملية الحفظ التي تشير إليها هذه الحقول هي الحفظ اليدوي في تطبيق مثل Microsoft Word،
// ليست طريقة حفظ المستند.
// فيما يلي ثلاثة أنواع مختلفة من التقويم والتي وفقًا لها يمكن لحقل SAVEDATE عرض التاريخ/الوقت.
// 1 - التقويم القمري الإسلامي:
builder.Write("According to the Lunar Calendar - ");
FieldSaveDate field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" SAVEDATE  \\h", field.GetFieldCode());

// 2 - تقويم أم القرى:
builder.Write("\nAccording to the Umm al-Qura calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\u", field.GetFieldCode());

// 3 - التقويم الوطني الهندي:
builder.Write("\nAccording to the Indian National calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\s", field.GetFieldCode());

// تستمد حقول SAVEDATE قيم التاريخ/الوقت الخاصة بها من الخاصية المضمنة LastSavedTime.
// لن تقوم طريقة حفظ المستند بتحديث هذه القيمة، ولكن لا يزال بإمكاننا تحديثها يدويًا.
doc.BuiltInDocumentProperties.LastSavedTime = DateTime.Now;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SAVEDATE.docx");
```

### أنظر أيضا

* class [FieldSaveDate](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
