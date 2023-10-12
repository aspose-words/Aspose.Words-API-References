---
title: Class FieldIf
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.FieldIf فصل. ينفذ حقل IF.
type: docs
weight: 2000
url: /ar/net/aspose.words.fields/fieldif/
---
## FieldIf class

ينفذ حقل IF.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

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
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | الحصول على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [FalseText](../../aspose.words.fields/fieldif/falsetext/) { get; set; } | الحصول على أو تعيين النص المعروض إذا كان تعبير المقارنة كذلك`خطأ شنيع` . |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/) الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تعيين ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | الحصول على أو تعيين ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب النتيجة). |
| [LeftExpression](../../aspose.words.fields/fieldif/leftexpression/) { get; set; } | الحصول على أو تعيين الجزء الأيسر من تعبير المقارنة. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تعيين LCID الخاص بالحقل. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [RightExpression](../../aspose.words.fields/fieldif/rightexpression/) { get; set; } | الحصول على أو تعيين الجزء الأيمن من تعبير المقارنة. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقول. يمكن ان يكون`باطل` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [TrueText](../../aspose.words.fields/fieldif/truetext/) { get; set; } | الحصول على النص المعروض أو تعيينه إذا كان تعبير المقارنة صحيحًا. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | الحصول على نوع حقل Microsoft Word. |

## طُرق

| اسم | وصف |
| --- | --- |
| [EvaluateCondition](../../aspose.words.fields/fieldif/evaluatecondition/)() | تقييم الحالة. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | إزالة الحقل من المستند. إرجاع عقدة مباشرة بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير للعقدة الأصلية، فسيتم إرجاع الفقرة الأصلية الخاصة به. إذا تمت إزالة الحقل بالفعل، فسيتم إرجاعه`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يقوم بإجراء التحديث الميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(bool) | إجراء تحديث ميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |

### ملاحظات

يقارن القيم المعينة بواسطة التعبيرات[`LeftExpression`](./leftexpression/) و[`RightExpression`](./rightexpression/) بالمقارنة باستخدام عامل التشغيل المعين بواسطة[`ComparisonOperator`](./comparisonoperator/).

سيتم استخدام حقل بالتنسيق التالي كمصدر لدمج البريد: { IF 0 = 0 "{PatientsNameFML}" "" \* MERGEFORMAT }

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

// سيعرض حقل IF سلسلة من خاصية "TrueText" الخاصة به،
// أو خاصية "FalseText" الخاصة بها، اعتمادًا على صحة العبارة التي قمنا ببنائها.
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// في هذه الحالة، "0 = 1" غير صحيح، لذا ستكون النتيجة المعروضة "خطأ".
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

// هذه المرة العبارة صحيحة، لذا ستكون النتيجة المعروضة "صحيح".
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


