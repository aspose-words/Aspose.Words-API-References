---
title: FieldListNum Class
linktitle: FieldListNum
articleTitle: FieldListNum
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.FieldListNum لتطبيق سلس لحقول LISTNUM. حسّن أتمتة المستندات بميزات فعّالة اليوم!
type: docs
weight: 2530
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
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/)الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [HasListName](../../aspose.words.fields/fieldlistnum/haslistname/) { get; } | ترجع قيمة تشير إلى ما إذا كان اسم تعريف الترقيم المجرد يتم توفيره بواسطة كود الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | يحصل على أو يحدد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | يحصل على أو يحدد ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب نتيجته). |
| [ListLevel](../../aspose.words.fields/fieldlistnum/listlevel/) { get; set; } | يحصل على المستوى الموجود في القائمة أو يعينه، متجاوزًا السلوك الافتراضي للحقل. |
| [ListName](../../aspose.words.fields/fieldlistnum/listname/) { get; set; } | يحصل على اسم تعريف الترقيم المجرد المستخدم للترقيم أو يعينه. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | يحصل على أو يعين LCID للحقل. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | يحصل على النص الموجود بين فاصل الحقل ونهاية الحقل أو يعينه. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن يكون`باطل` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [StartingNumber](../../aspose.words.fields/fieldlistnum/startingnumber/) { get; set; } | يحصل على القيمة الأولية لهذا الحقل أو يعينها. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | يحصل على نوع حقل Microsoft Word. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | يُزيل الحقل من المستند. يُرجع عقدة بعد الحقل مباشرةً. إذا كانت نهاية الحقل هي آخر عقدة فرعية للعقدة الأصلية، تُرجع فقرته الأصلية. إذا كان الحقل قد حُذف مُسبقًا، تُرجع`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يُجري تحديث الحقل. يُطرح هذا الخطأ إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | يُجري تحديثًا للحقل. يُطرح هذا الخطأ إذا كان الحقل قيد التحديث بالفعل. |

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

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
