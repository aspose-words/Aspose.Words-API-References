---
title: FieldAdvance Class
linktitle: FieldAdvance
articleTitle: FieldAdvance
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.FieldAdvance لتنفيذ حقل ADVANCE بسلاسة، مما يعزز قدرات معالجة المستندات لديك دون عناء.
type: docs
weight: 1950
url: /ar/net/aspose.words.fields/fieldadvance/
---
## FieldAdvance class

ينفذ حقل ADVANCE.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldAdvance : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldAdvance](fieldadvance/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [DownOffset](../../aspose.words.fields/fieldadvance/downoffset/) { get; set; } | يحصل على عدد النقاط التي يجب أن يتحرك بها النص الذي يلي الحقل إلى الأسفل أو يعينه. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/)الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [HorizontalPosition](../../aspose.words.fields/fieldadvance/horizontalposition/) { get; set; } | يحصل على أو يعين عدد النقاط التي يجب نقل النص الذي يتبع الحقل أفقيًا من الحافة اليسرى للعمود أو الإطار أو مربع النص. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | يحصل على أو يحدد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | يحصل على أو يحدد ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب نتيجته). |
| [LeftOffset](../../aspose.words.fields/fieldadvance/leftoffset/) { get; set; } | يحصل على عدد النقاط التي يجب أن يتحرك بها النص الذي يلي الحقل إلى اليسار أو يعينه. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | يحصل على أو يعين LCID للحقل. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | يحصل على النص الموجود بين فاصل الحقل ونهاية الحقل أو يعينه. |
| [RightOffset](../../aspose.words.fields/fieldadvance/rightoffset/) { get; set; } | يحصل على عدد النقاط التي يجب أن يتحرك بها النص الذي يلي الحقل إلى اليمين أو يعينه. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن يكون`باطل` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | يحصل على نوع حقل Microsoft Word. |
| [UpOffset](../../aspose.words.fields/fieldadvance/upoffset/) { get; set; } | يحصل على عدد النقاط التي يجب أن يتحرك بها النص الذي يلي الحقل لأعلى أو يعينها. |
| [VerticalPosition](../../aspose.words.fields/fieldadvance/verticalposition/) { get; set; } | يحصل على أو يعين عدد النقاط التي يجب أن يتحرك بها النص الذي يتبع الحقل عموديًا من الحافة العلوية للصفحة. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | يُزيل الحقل من المستند. يُرجع عقدة بعد الحقل مباشرةً. إذا كانت نهاية الحقل هي آخر عقدة فرعية للعقدة الأصلية، تُرجع فقرته الأصلية. إذا كان الحقل قد حُذف مُسبقًا، تُرجع`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يُجري تحديث الحقل. يُطرح هذا الخطأ إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | يُجري تحديثًا للحقل. يُطرح هذا الخطأ إذا كان الحقل قيد التحديث بالفعل. |

## ملاحظات

يحرك نقطة البداية التي يتم عندها عرض النص الذي يتبع الحقل معجميًا إلى اليمين أو اليسار، أو إلى الأعلى أو الأسفل، أو إلى موضع أفقي أو رأسي محدد.

## أمثلة

يوضح كيفية إدراج حقل ADVANCE وتحرير خصائصه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// فيما يلي طريقتان لاستخدام الحقل ADVANCE لتعديل موضع النص الذي يليه.
// تستمر تأثيرات حقل ADVANCE في التطبيق حتى نهاية الفقرة،
// أو يقوم حقل ADVANCE آخر بتحديث قيم الإزاحة/الإحداثيات.
// 1 - تحديد الإزاحة الاتجاهية:
FieldAdvance field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.RightOffset = "5";
field.UpOffset = "5";

Assert.AreEqual(" ADVANCE  \\r 5 \\u 5", field.GetFieldCode());

builder.Write("This text will be moved up and to the right.");

field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.DownOffset = "5";
field.LeftOffset = "100";

Assert.AreEqual(" ADVANCE  \\d 5 \\l 100", field.GetFieldCode());

builder.Writeln("This text is moved down and to the left, overlapping the previous text.");

// 2 - نقل النص إلى موضع محدد بواسطة الإحداثيات:
field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.HorizontalPosition = "-100";
field.VerticalPosition = "200";

Assert.AreEqual(" ADVANCE  \\x -100 \\y 200", field.GetFieldCode());

builder.Write("This text is in a custom position.");

doc.Save(ArtifactsDir + "Field.ADVANCE.docx");
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
