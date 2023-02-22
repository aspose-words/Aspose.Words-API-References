---
title: FieldSaveDate.UseUmAlQuraCalendar
second_title: Aspose.Words لمراجع .NET API
description: FieldSaveDate ملكية. الحصول على أو تحديد ما إذا كان سيتم استخدام تقويم أم القرى.
type: docs
weight: 40
url: /ar/net/aspose.words.fields/fieldsavedate/useumalquracalendar/
---
## FieldSaveDate.UseUmAlQuraCalendar property

الحصول على أو تحديد ما إذا كان سيتم استخدام تقويم أم القرى.

```csharp
public bool UseUmAlQuraCalendar { get; set; }
```

### أمثلة

يوضح كيفية استخدام حقل الحفظ لعرض تاريخ / وقت أحدث عملية حفظ للمستند تم إجراؤها باستخدام Microsoft Word.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was last saved:");

// يمكننا استخدام حقل الحفظ لعرض تاريخ ووقت آخر عملية حفظ على المستند.
// عملية الحفظ التي تشير إليها هذه الحقول هي الحفظ اليدوي في تطبيق مثل Microsoft Word ،
// ليست طريقة حفظ المستند.
// فيما يلي ثلاثة أنواع مختلفة من التقويمات والتي وفقًا لحقل "حفظ" يمكن أن يعرض التاريخ / الوقت.
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

// ترسم حقول الحفظ قيم التاريخ / الوقت من خاصية LastSavedTime المضمنة.
// لن تقوم طريقة حفظ المستند بتحديث هذه القيمة ، ولكن لا يزال بإمكاننا تحديثها يدويًا.
doc.BuiltInDocumentProperties.LastSavedTime = DateTime.Now;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SAVEDATE.docx");
```

### أنظر أيضا

* class [FieldSaveDate](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldsavedate/)
* المجسم [Aspose.Words](../../../)


