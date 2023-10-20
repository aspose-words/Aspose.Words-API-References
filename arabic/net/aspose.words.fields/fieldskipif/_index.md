---
title: FieldSkipIf Class
linktitle: FieldSkipIf
articleTitle: FieldSkipIf
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fields.FieldSkipIf فصل. تنفيذ حقل SKIPIF في C#.
type: docs
weight: 2420
url: /ar/net/aspose.words.fields/fieldskipif/
---
## FieldSkipIf class

تنفيذ حقل SKIPIF.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldSkipIf : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldSkipIf](fieldskipif/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldskipif/comparisonoperator/) { get; set; } | الحصول على عامل المقارنة أو تعيينه. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | الحصول على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/) الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تعيين ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | الحصول على أو تعيين ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب النتيجة). |
| [LeftExpression](../../aspose.words.fields/fieldskipif/leftexpression/) { get; set; } | الحصول على أو تعيين الجزء الأيسر من تعبير المقارنة. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تعيين LCID الخاص بالحقل. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [RightExpression](../../aspose.words.fields/fieldskipif/rightexpression/) { get; set; } | الحصول على أو تعيين الجزء الأيمن من تعبير المقارنة. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقول. يمكن ان يكون`باطل` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | الحصول على نوع حقل Microsoft Word. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | إزالة الحقل من المستند. إرجاع عقدة مباشرة بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير للعقدة الأصلية، فسيتم إرجاع الفقرة الأصلية الخاصة به. إذا تمت إزالة الحقل بالفعل، فسيتم إرجاعه`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يقوم بإجراء التحديث الميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | إجراء تحديث ميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |

## ملاحظات

يقارن القيم المعينة بالتعبيرات[`LeftExpression`](./leftexpression/) و[`RightExpression`](./rightexpression/) بالمقارنة باستخدام عامل التشغيل المعين بواسطة[`ComparisonOperator`](./comparisonoperator/) . إذا كانت المقارنة صحيحة، فإن SKIPIF يلغي مستند الدمج الحالي، وينتقل إلى سجل البيانات التالي في مصدر البيانات، ويبدأ مستند دمج جديد. إذا كانت المقارنة خاطئة، فسيتم متابعة مستند الدمج الحالي.

## أمثلة

يوضح كيفية تخطي الصفحات في عملية دمج البريد باستخدام حقل SKIPIF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقل SKIPIF. إذا كان الصف الحالي لعملية دمج المراسلات يحقق الشرط
// حالة تعبيرات هذا الحقل، ثم تقوم عملية دمج المراسلات بإحباط الصف الحالي،
// يتجاهل مستند الدمج الحالي، ثم ينتقل فورًا إلى الصف التالي لبدء مستند الدمج التالي.
FieldSkipIf fieldSkipIf = (FieldSkipIf) builder.InsertField(FieldType.FieldSkipIf, true);

// انقل المنشئ إلى فاصل حقل SKIPIF حتى نتمكن من وضع MERGEFIELD داخل حقل SKIPIF.
builder.MoveTo(fieldSkipIf.Separator);
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Department";

// يشير MERGEFIELD إلى عمود "القسم" في جدول البيانات الخاص بنا. إذا كان هناك صف من هذا الجدول
// يحتوي على قيمة "HR" في عمود "القسم" الخاص به، وهذا الصف سوف يحقق الشرط.
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "HR";

// أضف محتوى إلى وثيقتنا، وأنشئ مصدر البيانات، وقم بتنفيذ دمج المراسلات.
builder.MoveToDocumentEnd();
builder.Write("Dear ");
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(", ");

 // يحتوي هذا الجدول على ثلاثة صفوف، واحد منهم يفي بشرط حقل SKIPIF الخاص بنا.
// سيؤدي دمج البريد إلى إنتاج صفحتين.
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Columns.Add("Department");
table.Rows.Add("John Doe", "Sales");
table.Rows.Add("Jane Doe", "Accounting");
table.Rows.Add("John Cardholder", "HR");

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.SKIPIF.docx");
```

يوضح كيفية استخدام حقلي MERGEREC وMERGESEQ لعدد سجلات دمج البريد وعددها في مستندات إخراج دمج البريد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(",");

// سيطبع حقل MERGEREC رقم صف البيانات التي يتم دمجها في كل مستند إخراج مدمج.
builder.Write("\nRow number of record in data source: ");
FieldMergeRec fieldMergeRec = (FieldMergeRec)builder.InsertField(FieldType.FieldMergeRec, true);

Assert.AreEqual(" MERGEREC ", fieldMergeRec.GetFieldCode());

// سيحسب حقل MERGESEQ عدد عمليات الدمج الناجحة ويطبع القيمة الحالية في كل صفحة على حدة.
// إذا كانت عملية دمج البريد لا تتخطى أي صفوف ولا تستدعي أي حقول SKIP/SKIPIF/NEXT/NEXTIF، فستكون كافة عمليات الدمج ناجحة.
// سيعرض حقلا MERGESEQ وMERGEREC نفس نتائج دمج البريد الخاص بهما بنجاح.
builder.Write("\nSuccessful merge number: ");
FieldMergeSeq fieldMergeSeq = (FieldMergeSeq)builder.InsertField(FieldType.FieldMergeSeq, true);

Assert.AreEqual(" MERGESEQ ", fieldMergeSeq.GetFieldCode());

// أدخل حقل SKIPIF، والذي سيتخطى عملية الدمج إذا كان الاسم "John Doe".
FieldSkipIf fieldSkipIf = (FieldSkipIf)builder.InsertField(FieldType.FieldSkipIf, true);
builder.MoveTo(fieldSkipIf.Separator);
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "John Doe";

// قم بإنشاء مصدر بيانات مكون من 3 صفوف، يحتوي أحدهم على "John Doe" كقيمة لعمود "الاسم".
// نظرًا لأنه سيتم تشغيل حقل SKIPIF مرة واحدة بهذه القيمة، فإن مخرجات دمج البريد لدينا ستحتوي على صفحتين بدلاً من 3.
// في الصفحة 1، سيعرض كل من حقلي MERGESEQ وMERGEREC الرقم "1".
// في الصفحة 2، سيعرض حقل MERGEREC "3" وسيعرض حقل MERGESEQ "2".
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Rows.Add(new[] { "Jane Doe" });
table.Rows.Add(new[] { "John Doe" });
table.Rows.Add(new[] { "Joe Bloggs" });

doc.MailMerge.Execute(table);            
doc.Save(ArtifactsDir + "Field.MERGEREC.MERGESEQ.docx");
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
