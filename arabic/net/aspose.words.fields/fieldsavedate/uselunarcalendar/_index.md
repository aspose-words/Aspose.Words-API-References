---
title: FieldSaveDate.UseLunarCalendar
second_title: Aspose.Words لمراجع .NET API
description: FieldSaveDate ملكية. الحصول على أو تحديد ما إذا كان سيتم استخدام التقويم القمري الهجري أو القمري العبري.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldsavedate/uselunarcalendar/
---
## FieldSaveDate.UseLunarCalendar property

الحصول على أو تحديد ما إذا كان سيتم استخدام التقويم القمري الهجري أو القمري العبري.

```csharp
public bool UseLunarCalendar { get; set; }
```

### أمثلة

يوضح كيفية استخدام الحقل "حفظ" لعرض تاريخ/وقت آخر عملية حفظ للمستند تم تنفيذها باستخدام Microsoft Word.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was last saved:");

// يمكننا استخدام حقل الحفظ لعرض تاريخ ووقت عملية الحفظ الأخيرة على المستند.
// عملية الحفظ التي تشير إليها هذه الحقول هي عملية الحفظ اليدوي في تطبيق مثل Microsoft Word،
// ليست طريقة حفظ المستند.
// فيما يلي ثلاثة أنواع تقويم مختلفة يمكن لحقل الحفظ وفقًا لها عرض التاريخ/الوقت.
// 1 - التقويم القمري الإسلامي:
builder.Write("According to the Lunar Calendar - ");
FieldSaveDate field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" SAVEDATE  \\h", field.GetFieldCode());

// 2 - تقويم أم القرى :
builder.Write("\nAccording to the Umm al-Qura calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\u", field.GetFieldCode());

// 3 - التقويم الوطني الهندي:
builder.Write("\nAccording to the Indian National calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\s", field.GetFieldCode());

// ترسم حقول SAVEDATE قيم التاريخ/الوقت الخاصة بها من خاصية LastSavedTime المضمنة.
// لن تقوم طريقة حفظ المستند بتحديث هذه القيمة، ولكن لا يزال بإمكاننا تحديثها يدويًا.
doc.BuiltInDocumentProperties.LastSavedTime = DateTime.Now;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SAVEDATE.docx");
```

### أنظر أيضا

* class [FieldSaveDate](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldsavedate/)
* المجسم [Aspose.Words](../../../)


