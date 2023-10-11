---
title: FieldListNum.ListName
second_title: Aspose.Words لمراجع .NET API
description: FieldListNum ملكية. الحصول على أو تعيين اسم تعريف الترقيم المجرد المستخدم للترقيم.
type: docs
weight: 40
url: /ar/net/aspose.words.fields/fieldlistnum/listname/
---
## FieldListNum.ListName property

الحصول على أو تعيين اسم تعريف الترقيم المجرد المستخدم للترقيم.

```csharp
public string ListName { get; set; }
```

### أمثلة

يوضح كيفية ترقيم الفقرات باستخدام حقول LISTNUM.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تعرض حقول LISTNUM رقمًا يتزايد في كل حقل LISTNUM.
// تحتوي هذه الحقول أيضًا على مجموعة متنوعة من الخيارات التي تسمح لنا باستخدامها لمحاكاة القوائم المرقمة.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// تبدأ القوائم بالعد عند 1 افتراضيًا، ولكن يمكننا ضبط هذا الرقم على قيمة مختلفة، مثل 0.
// سيعرض هذا الحقل "0)".
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

 // تحتفظ حقول LISTNUM بأعداد منفصلة لكل مستوى قائمة.
// إدراج حقل LISTNUM في نفس الفقرة كحقل LISTNUM آخر
// يزيد مستوى القائمة بدلاً من العدد.
// سيواصل الحقل التالي العد الذي بدأناه أعلاه وسيعرض القيمة "1" على مستوى القائمة 1.
builder.InsertField(FieldType.FieldListNum, true);

// سيبدأ هذا الحقل العد على مستوى القائمة 2. وسيعرض القيمة "1".
builder.InsertField(FieldType.FieldListNum, true);

// سيبدأ هذا الحقل العد على مستوى القائمة 3. وسيعرض القيمة "1".
// مستويات القائمة المختلفة لها تنسيق مختلف،
// لذلك ستعرض هذه الحقول المدمجة قيمة "1)a)i)".
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// سيستمر حقل LISTNUM التالي الذي نقوم بإدراجه في العد على مستوى القائمة
// أن حقل LISTNUM السابق كان قيد التشغيل.
// يمكننا استخدام خاصية "ListLevel" للانتقال إلى مستوى قائمة مختلف.
// إذا ظل حقل LISTNUM هذا في مستوى القائمة 3، فسيتم عرض "ii)"،
// ولكن بما أننا نقلناه إلى مستوى القائمة 2، فإنه يستمر في العد عند هذا المستوى ويعرض "ب)".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// يمكننا تعيين خاصية ListName للحصول على الحقل لمحاكاة نوع حقل AUTONUM مختلف.
// "NumberDefault" يحاكي AUTONUM، و"OutlineDefault" يحاكي AUTONUMOUT،
// و"LegalDefault" يحاكي حقول AUTONUMLGL.
// اسم القائمة "OutlineDefault" الذي يحتوي على 1 كرقم البداية سيؤدي إلى عرض "I.".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// لا ينتقل اسم القائمة من الحقل السابق، لذا سنحتاج إلى تعيينه لكل حقل جديد.
// يستمر هذا الحقل في العد باسم قائمة مختلف ويعرض "II.".
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


