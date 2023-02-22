---
title: FieldListNum.HasListName
second_title: Aspose.Words لمراجع .NET API
description: FieldListNum ملكية. إرجاع قيمة تشير إلى ما إذا كان اسم تعريف الترقيم المجرد مقدمًا من خلال رمز الحقل.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldlistnum/haslistname/
---
## FieldListNum.HasListName property

إرجاع قيمة تشير إلى ما إذا كان اسم تعريف الترقيم المجرد مقدمًا من خلال رمز الحقل.

```csharp
public bool HasListName { get; }
```

### أمثلة

يوضح كيفية ترقيم الفقرات باستخدام حقول LISTNUM.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تعرض حقول LISTNUM رقمًا يتزايد في كل حقل LISTNUM.
// تحتوي هذه الحقول أيضًا على مجموعة متنوعة من الخيارات التي تتيح لنا استخدامها لمحاكاة القوائم المرقمة.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// تبدأ القوائم في العد عند 1 افتراضيًا ، ولكن يمكننا تعيين هذا الرقم على قيمة مختلفة ، مثل 0.
// سيعرض هذا الحقل "0)".
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

 // تحتفظ حقول LISTNUM بأعداد منفصلة لكل مستوى قائمة.
// إدراج حقل LISTNUM في نفس الفقرة مثل حقل LISTNUM آخر
// يزيد من مستوى القائمة بدلاً من العدد.
// سيستمر الحقل التالي في العد الذي بدأناه أعلاه ويعرض القيمة "1" في مستوى القائمة 1.
builder.InsertField(FieldType.FieldListNum, true);

// سيبدأ هذا الحقل في العد عند مستوى القائمة 2. وسيعرض القيمة "1".
builder.InsertField(FieldType.FieldListNum, true);

// سيبدأ هذا الحقل في العد عند مستوى القائمة 3. وسيعرض القيمة "1".
// مستويات القائمة المختلفة لها تنسيق مختلف ،
// لذلك ستعرض هذه الحقول مجتمعة قيمة "1) أ) ط)".
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// سيواصل حقل LISTNUM التالي الذي ندرجه العد على مستوى القائمة
// أن حقل LISTNUM السابق كان قيد التشغيل.
// يمكننا استخدام خاصية "ListLevel" للانتقال إلى مستوى قائمة مختلف.
// إذا ظل حقل LISTNUM هذا في مستوى القائمة 3 ، فسيتم عرض "ii)" ،
// ولكن نظرًا لأننا نقلناه إلى مستوى القائمة 2 ، فإنه يستمر في العد عند هذا المستوى ويعرض "ب)".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// يمكننا تعيين خاصية ListName للحصول على الحقل لمضاهاة نوع حقل AUTONUM مختلف.
// "NumberDefault" يحاكي AUTONUM ، "OutlineDefault" يحاكي AUTONUMOUT ،
// و "LegalDefault" يحاكي حقول AUTONUMLGL.
// اسم القائمة "OutlineDefault" مع 1 كرقم البداية سينتج عنه عرض "I.".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// لا ينتقل ListName من الحقل السابق ، لذلك سنحتاج إلى تعيينه لكل حقل جديد.
// هذا الحقل يواصل العد باسم قائمة مختلف ويعرض "II.".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 5");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.LISTNUM.docx");
```

### أنظر أيضا

* class [FieldListNum](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldlistnum/)
* المجسم [Aspose.Words](../../../)


