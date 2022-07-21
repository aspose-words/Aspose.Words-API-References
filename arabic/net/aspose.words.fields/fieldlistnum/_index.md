---
title: FieldListNum
second_title: Aspose.Words لمراجع .NET API
description: تنفذ حقل LISTNUM .
type: docs
weight: 1970
url: /ar/net/aspose.words.fields/fieldlistnum/
---
## FieldListNum class

تنفذ حقل LISTNUM .

```csharp
public class FieldListNum : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldListNum](fieldlistnum)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format) { get; } | يحصل على أ[`FieldFormat`](../fieldformat) كائن يوفر وصولاً مكتوبًا إلى تنسيق الحقل. |
| [HasListName](../../aspose.words.fields/fieldlistnum/haslistname) { get; } | إرجاع قيمة تشير إلى ما إذا كان اسم تعريف الترقيم المجرد مقدمًا من خلال رمز الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | تحديد ما إذا كان الحقل مغلقًا أم لا (يجب عدم إعادة حساب النتيجة). |
| [ListLevel](../../aspose.words.fields/fieldlistnum/listlevel) { get; set; } | الحصول على المستوى في القائمة أو تعيينه ، متجاوزًا السلوك الافتراضي للحقل. |
| [ListName](../../aspose.words.fields/fieldlistnum/listname) { get; set; } | الحصول على أو تحديد اسم تعريف الترقيم المجرد المستخدم للترقيم. |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | الحصول على أو تحديد LCID للحقل. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | يحصل على العقدة التي تمثل فاصل المجال. يمكن أن يكون فارغًا. |
| [Start](../../aspose.words.fields/field/start) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [StartingNumber](../../aspose.words.fields/fieldlistnum/startingnumber) { get; set; } | الحصول على أو تعيين قيمة البداية لهذا الحقل. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | يحصل على نوع حقل Microsoft Word . |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . |
| [Remove](../../aspose.words.fields/field/remove)() | يزيل الحقل من المستند. إرجاع عقدة بعد الحقل مباشرة. إذا كانت نهاية الحقل هي آخر child من العقدة الأصلية ، يتم إرجاع فقرته الأصلية. إذا تمت إزالة الحقل بالفعل ، يعود **لا شيء** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update)() | يقوم بالتحديث الميداني. يرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update)(bool) | يقوم بإجراء تحديث ميداني. يرمي إذا تم تحديث الحقل بالفعل. |

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

* class [Field](../field)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
