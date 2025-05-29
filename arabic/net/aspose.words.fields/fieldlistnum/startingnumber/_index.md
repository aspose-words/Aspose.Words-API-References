---
title: FieldListNum.StartingNumber
linktitle: StartingNumber
articleTitle: StartingNumber
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldListNum StartingNumber لإدارة قيمة بدء الحقل بسهولة لتحسين تنظيم البيانات وكفاءتها.
type: docs
weight: 50
url: /ar/net/aspose.words.fields/fieldlistnum/startingnumber/
---
## FieldListNum.StartingNumber property

يحصل على القيمة الأولية لهذا الحقل أو يعينها.

```csharp
public string StartingNumber { get; set; }
```

## أمثلة

يوضح كيفية ترقيم الفقرات باستخدام حقول LISTNUM.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تعرض حقول LISTNUM رقمًا يتزايد في كل حقل LISTNUM.
//تحتوي هذه الحقول أيضًا على مجموعة متنوعة من الخيارات التي تسمح لنا باستخدامها لمحاكاة القوائم المرقمة.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// تبدأ القوائم بالعد عند 1 بشكل افتراضي، ولكن يمكننا تعيين هذا الرقم إلى قيمة مختلفة، مثل 0.
//سيتم عرض هذا الحقل "0)".
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

// تحتفظ حقول LISTNUM بأعداد منفصلة لكل مستوى من مستويات القائمة.
// إدراج حقل LISTNUM في نفس الفقرة مع حقل LISTNUM آخر
// يزيد مستوى القائمة بدلاً من العدد.
// سيستمر الحقل التالي في العد الذي بدأناه أعلاه ويعرض قيمة "1" على مستوى القائمة 1.
builder.InsertField(FieldType.FieldListNum, true);

// سيبدأ هذا الحقل العد على مستوى القائمة 2. وسيعرض القيمة "1".
builder.InsertField(FieldType.FieldListNum, true);

// سيبدأ هذا الحقل العد على مستوى القائمة 3. وسيعرض القيمة "1".
// مستويات القائمة المختلفة لها تنسيق مختلف،
// لذلك فإن دمج هذه الحقول سيؤدي إلى عرض قيمة "1)a)i)".
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// الحقل LISTNUM التالي الذي نقوم بإدخاله سيستمر في العد على مستوى القائمة
// أن الحقل LISTNUM السابق كان موجودًا.
//يمكننا استخدام خاصية "ListLevel" للانتقال إلى مستوى قائمة مختلف.
// إذا بقي حقل LISTNUM هذا على مستوى القائمة 3، فسوف يعرض "ii)"،
// ولكن، نظرًا لأننا نقلناها إلى مستوى القائمة 2، فإنها تستمر في العد على هذا المستوى وتعرض "ب)".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// يمكننا تعيين خاصية ListName لجعل الحقل يحاكي نوع حقل AUTONUM مختلفًا.
// "NumberDefault" يحاكي AUTONUM، و"OutlineDefault" يحاكي AUTONUMOUT،
// و"LegalDefault" يحاكي حقول AUTONUMLGL.
// سيؤدي اسم القائمة "OutlineDefault" مع 1 كرقم بداية إلى عرض "I".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// لا يتم نقل ListName من الحقل السابق، لذا سنحتاج إلى تعيينه لكل حقل جديد.
// يواصل هذا الحقل العد باستخدام اسم القائمة المختلفة ويعرض "II".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 5");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.LISTNUM.docx");
```

### أنظر أيضا

* class [FieldListNum](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
