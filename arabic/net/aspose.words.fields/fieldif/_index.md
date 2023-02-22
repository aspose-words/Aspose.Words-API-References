---
title: Class FieldIf
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.FieldIf فصل. تنفذ حقل IF .
type: docs
weight: 1850
url: /ar/net/aspose.words.fields/fieldif/
---
## FieldIf class

تنفذ حقل IF .

```csharp
public class FieldIf : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldIf](fieldif/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldif/comparisonoperator/) { get; set; } | الحصول على عامل المقارنة أو تعيينه. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [FalseText](../../aspose.words.fields/fieldif/falsetext/) { get; set; } | الحصول على النص المعروض أو تحديده إذا كان تعبير المقارنة خاطئًا . |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على أ[`FieldFormat`](../fieldformat/) كائن يوفر وصولاً مكتوبًا إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | تحديد ما إذا كان الحقل مغلقًا أم لا (يجب عدم إعادة حساب النتيجة). |
| [LeftExpression](../../aspose.words.fields/fieldif/leftexpression/) { get; set; } | الحصول على أو تعيين الجزء الأيسر من تعبير المقارنة. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تحديد LCID للحقل. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [RightExpression](../../aspose.words.fields/fieldif/rightexpression/) { get; set; } | الحصول على الجزء الصحيح من تعبير المقارنة أو تعيينه. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل المجال. يمكن أن يكون فارغًا. |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [TrueText](../../aspose.words.fields/fieldif/truetext/) { get; set; } | الحصول على النص المعروض أو تعيينه إذا كان تعبير المقارنة صحيحًا. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | يحصل على نوع حقل Microsoft Word . |

## طُرق

| اسم | وصف |
| --- | --- |
| [EvaluateCondition](../../aspose.words.fields/fieldif/evaluatecondition/)() | يقيم الحالة. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . |
| [Remove](../../aspose.words.fields/field/remove/)() | يزيل الحقل من المستند. إرجاع عقدة بعد الحقل مباشرة. إذا كانت نهاية الحقل هي آخر child من العقدة الأصلية ، يتم إرجاع فقرته الأصلية. إذا تمت إزالة الحقل بالفعل ، يعود **لا شيء** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يقوم بالتحديث الميداني. يرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(bool) | يقوم بإجراء تحديث ميداني. يرمي إذا تم تحديث الحقل بالفعل. |

### ملاحظات

يقارن القيم المعينة بواسطة التعبيرات[`LeftExpression`](./leftexpression/) و[`RightExpression`](./rightexpression/) بالمقارنة باستخدام المشغل المعين من قبل[`ComparisonOperator`](./comparisonoperator/).

سيتم استخدام حقل بالتنسيق التالي كمصدر لدمج البريد: {IF 0 = 0 "{PatientsNameFML}" "" \ * MERGEFORMAT}

### أمثلة

يوضح كيفية إدراج حقل IF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Statement 1: ");
FieldIf field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "0";
field.ComparisonOperator = "=";
field.RightExpression = "1";

// سيعرض الحقل IF سلسلة من خاصية "TrueText" الخاصة به ،
// أو خاصيته "FalseText" ، اعتمادًا على حقيقة البيان الذي أنشأناه.
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// في هذه الحالة ، "0 = 1" غير صحيحة ، لذا ستكون النتيجة المعروضة "False".
Assert.AreEqual(" IF  0 = 1 True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.False, field.EvaluateCondition());
Assert.AreEqual("False", field.Result);

builder.Write("\nStatement 2: ");
field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "5";
field.ComparisonOperator = "=";
field.RightExpression = "2 + 3";
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// هذه المرة العبارة صحيحة ، لذا ستكون النتيجة المعروضة "صحيحة".
Assert.AreEqual(" IF  5 = \"2 + 3\" True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.True, field.EvaluateCondition());
Assert.AreEqual("True", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IF.docx");
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)


