---
title: FieldMergeField Class
linktitle: FieldMergeField
articleTitle: FieldMergeField
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.FieldMergeField لأتمتة مستندات سلسة. حسّن سير عملك باستخدام وظيفة MERGEFIELD الفعّالة.
type: docs
weight: 2560
url: /ar/net/aspose.words.fields/fieldmergefield/
---
## FieldMergeField class

ينفذ حقل MERGEFIELD.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldMergeField : Field
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [FieldName](../../aspose.words.fields/fieldmergefield/fieldname/) { get; set; } | يحصل على اسم حقل البيانات أو يعينه. |
| [FieldNameNoPrefix](../../aspose.words.fields/fieldmergefield/fieldnamenoprefix/) { get; } | يُرجع اسم حقل البيانات فقط. تُحذف أي بادئة من خاصية البادئة. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/)الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | يحصل على أو يحدد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | يحصل على أو يحدد ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب نتيجته). |
| [IsMapped](../../aspose.words.fields/fieldmergefield/ismapped/) { get; set; } | يحصل على أو يحدد ما إذا كان هذا الحقل حقلًا معينًا. |
| [IsVerticalFormatting](../../aspose.words.fields/fieldmergefield/isverticalformatting/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم تمكين تحويل الأحرف للتنسيق الرأسي. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | يحصل على أو يعين LCID للحقل. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | يحصل على النص الموجود بين فاصل الحقل ونهاية الحقل أو يعينه. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن يكون`باطل` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [TextAfter](../../aspose.words.fields/fieldmergefield/textafter/) { get; set; } | يحصل على النص الذي سيتم إدراجه بعد الحقل أو يعينه إذا لم يكن الحقل فارغًا. |
| [TextBefore](../../aspose.words.fields/fieldmergefield/textbefore/) { get; set; } | يحصل على النص الذي سيتم إدراجه قبل الحقل أو يعينه إذا لم يكن الحقل فارغًا. |
| override [Type](../../aspose.words.fields/fieldmergefield/type/) { get; } | يحصل على نوع حقل Microsoft Word. |

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

يسترد اسم حقل البيانات ضمن أحرف الدمج في مستند رئيسي لدمج البريد. عندما يتم دمج المستند الرئيسي مع مصدر البيانات المحدد، يتم إدراج المعلومات من حقل البيانات المحدد بدلاً من حقل الدمج.

## أمثلة

يوضح كيفية استخدام حقول MERGEFIELD لإجراء دمج البريد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء جدول بيانات لاستخدامه كمصدر بيانات لدمج البريد.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// إدراج MERGEFIELD مع تعيين خاصية FieldName إلى اسم عمود في مصدر البيانات.
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Courtesy Title";
fieldMergeField.IsMapped = true;
fieldMergeField.IsVerticalFormatting = false;

//يمكننا تطبيق النص قبل وبعد القيمة التي يقبلها هذا الحقل عند حدوث الدمج.
fieldMergeField.TextBefore = "Dear ";
fieldMergeField.TextAfter = " ";

Assert.AreEqual(" MERGEFIELD  \"Courtesy Title\" \\m \\b \"Dear \" \\f \" \"", fieldMergeField.GetFieldCode());
Assert.AreEqual(FieldType.FieldMergeField, fieldMergeField.Type);

// أدخل MERGEFIELD آخر لعمود مختلف في مصدر البيانات.
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Last Name";
fieldMergeField.TextAfter = ":";

doc.UpdateFields();
doc.MailMerge.Execute(table);

Assert.AreEqual("Dear Mr. Doe:\u000cDear Mrs. Cardholder:", doc.GetText().Trim());
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
