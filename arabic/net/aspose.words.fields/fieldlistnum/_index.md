---
title: Class FieldListNum
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.FieldListNum فصل. ينفذ حقل LISTNUM.
type: docs
weight: 2120
url: /ar/net/aspose.words.fields/fieldlistnum/
---
## FieldListNum class

ينفذ حقل LISTNUM.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldListNum : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldListNum](fieldlistnum/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | الحصول على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/) الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [HasListName](../../aspose.words.fields/fieldlistnum/haslistname/) { get; } | إرجاع قيمة تشير إلى ما إذا كان اسم تعريف الترقيم المجرد مقدمًا بواسطة رمز الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تعيين ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | الحصول على أو تعيين ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب النتيجة). |
| [ListLevel](../../aspose.words.fields/fieldlistnum/listlevel/) { get; set; } | الحصول على المستوى في القائمة أو تعيينه، متجاوزًا السلوك الافتراضي للحقل. |
| [ListName](../../aspose.words.fields/fieldlistnum/listname/) { get; set; } | الحصول على أو تعيين اسم تعريف الترقيم المجرد المستخدم للترقيم. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تعيين LCID الخاص بالحقل. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقول. يمكن ان يكون`باطل` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [StartingNumber](../../aspose.words.fields/fieldlistnum/startingnumber/) { get; set; } | الحصول على أو تعيين قيمة البداية لهذا الحقل. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | الحصول على نوع حقل Microsoft Word. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | إزالة الحقل من المستند. إرجاع عقدة مباشرة بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير للعقدة الأصلية، فسيتم إرجاع الفقرة الأصلية الخاصة به. إذا تمت إزالة الحقل بالفعل، فسيتم إرجاعه`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يقوم بإجراء التحديث الميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(bool) | إجراء تحديث ميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |

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

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)


