---
title: FieldAdvance
second_title: Aspose.Words لمراجع .NET API
description: تنفذ حقل ADVANCE .
type: docs
weight: 1390
url: /ar/net/aspose.words.fields/fieldadvance/
---
## FieldAdvance class

تنفذ حقل ADVANCE .

```csharp
public class FieldAdvance : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldAdvance](fieldadvance)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروض. |
| [DownOffset](../../aspose.words.fields/fieldadvance/downoffset) { get; set; } | الحصول على أو تحديد عدد النقاط التي يجب نقل النص الذي يتبع الحقل إلى أسفل. |
| [End](../../aspose.words.fields/field/end) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format) { get; } | يحصل على أ[`FieldFormat`](../fieldformat) كائن يوفر وصولاً مكتوبًا إلى تنسيق الحقل. |
| [HorizontalPosition](../../aspose.words.fields/fieldadvance/horizontalposition) { get; set; } | الحصول على أو تحديد عدد النقاط التي يجب نقل النص الذي يتبع الحقل أفقيًا من الحافة اليسرى للعمود أو الإطار أو مربع النص. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | تحديد ما إذا كان الحقل مغلقًا أم لا (يجب عدم إعادة حساب النتيجة). |
| [LeftOffset](../../aspose.words.fields/fieldadvance/leftoffset) { get; set; } | الحصول على أو تحديد عدد النقاط التي يجب نقل النص الذي يتبع الحقل إلى اليسار. |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | الحصول على أو تحديد LCID للحقل. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [RightOffset](../../aspose.words.fields/fieldadvance/rightoffset) { get; set; } | الحصول على أو تحديد عدد النقاط التي يجب نقل النص الذي يتبع الحقل إلى اليمين . |
| [Separator](../../aspose.words.fields/field/separator) { get; } | يحصل على العقدة التي تمثل فاصل المجال. يمكن أن يكون فارغًا. |
| [Start](../../aspose.words.fields/field/start) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | يحصل على نوع حقل Microsoft Word . |
| [UpOffset](../../aspose.words.fields/fieldadvance/upoffset) { get; set; } | الحصول على أو تعيين عدد النقاط التي يجب نقل النص الذي يتبع الحقل لأعلى . |
| [VerticalPosition](../../aspose.words.fields/fieldadvance/verticalposition) { get; set; } | الحصول على أو تعيين عدد النقاط التي يجب نقل النص الذي يتبع الحقل عموديًا من الحافة العلوية للصفحة. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . |
| [Remove](../../aspose.words.fields/field/remove)() | يزيل الحقل من المستند. إرجاع عقدة بعد الحقل مباشرة. إذا كانت نهاية الحقل هي آخر child من العقدة الأصلية ، يتم إرجاع فقرته الأصلية. إذا تمت إزالة الحقل بالفعل ، يعود **لا شيء** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update)() | يقوم بالتحديث الميداني. يرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update)(bool) | يقوم بإجراء تحديث ميداني. يرمي إذا تم تحديث الحقل بالفعل. |

### ملاحظات

ينقل نقطة البداية التي يتم عندها عرض النص الذي يتبع الحقل معجمًا إلى اليمين أو اليسار ، لأعلى أو لأسفل ، أو إلى موضع أفقي أو رأسي محدد.

### أمثلة

يوضح كيفية إدراج حقل ADVANCE وتحرير خصائصه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// فيما يلي طريقتان لاستخدام حقل ADVANCE لضبط موضع النص الذي يليه.
// يستمر تطبيق تأثيرات حقل ADVANCE حتى تنتهي الفقرة ،
// أو يقوم حقل ADVANCE آخر بتحديث قيم الإزاحة / الإحداثيات.
// 1 - حدد إزاحة اتجاهية:
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

// 2 - نقل النص إلى الموضع المحدد بالإحداثيات:
field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.HorizontalPosition = "-100";
field.VerticalPosition = "200";

Assert.AreEqual(" ADVANCE  \\x -100 \\y 200", field.GetFieldCode());

builder.Write("This text is in a custom position.");

doc.Save(ArtifactsDir + "Field.ADVANCE.docx");
```

### أنظر أيضا

* class [Field](../field)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
