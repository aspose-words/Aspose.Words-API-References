---
title: FieldSkipIf Class
linktitle: FieldSkipIf
articleTitle: FieldSkipIf
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.FieldSkipIf لتنفيذ حقول SKIPIF بكفاءة، وتحسين أتمتة المستندات والمرونة في مشاريعك.
type: docs
weight: 2830
url: /ar/net/aspose.words.fields/fieldskipif/
---
## FieldSkipIf class

ينفذ حقل SKIPIF.

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
| [ComparisonOperator](../../aspose.words.fields/fieldskipif/comparisonoperator/) { get; set; } | يحصل على عامل المقارنة أو يعينه. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/)الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | يحصل على أو يحدد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | يحصل على أو يحدد ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب نتيجته). |
| [LeftExpression](../../aspose.words.fields/fieldskipif/leftexpression/) { get; set; } | يحصل على الجزء الأيسر من تعبير المقارنة أو يعينه. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | يحصل على أو يعين LCID للحقل. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | يحصل على النص الموجود بين فاصل الحقل ونهاية الحقل أو يعينه. |
| [RightExpression](../../aspose.words.fields/fieldskipif/rightexpression/) { get; set; } | يحصل على الجزء الصحيح من تعبير المقارنة أو يعينه. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن يكون`باطل` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
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

## ملاحظات

يقارن القيم المحددة بواسطة التعبيرات[`LeftExpression`](./leftexpression/) و[`RightExpression`](./rightexpression/) بالمقارنة باستخدام المشغل المعين بواسطة[`ComparisonOperator`](./comparisonoperator/) إذا كانت المقارنة صحيحة، يقوم SKIPIF بإلغاء مستند الدمج الحالي، وينتقل إلى سجل البيانات التالي في مصدر البيانات، ويبدأ مستند دمج جديدًا. إذا كانت المقارنة خاطئة، يستمر مستند الدمج الحالي.

## أمثلة

يوضح كيفية تخطي الصفحات في دمج البريد باستخدام الحقل SKIPIF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقل SKIPIF. إذا كان الصف الحالي لعملية دمج البريد يستوفي الشرط
// والتي تشير إليها تعبيرات هذا الحقل، ثم تقوم عملية دمج البريد بإلغاء الصف الحالي،
// يتجاهل مستند الدمج الحالي، ثم ينتقل على الفور إلى الصف التالي لبدء مستند الدمج التالي.
FieldSkipIf fieldSkipIf = (FieldSkipIf) builder.InsertField(FieldType.FieldSkipIf, true);

// نقل المنشئ إلى فاصل حقل SKIPIF حتى نتمكن من وضع MERGEFIELD داخل حقل SKIPIF.
builder.MoveTo(fieldSkipIf.Separator);
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Department";

// يشير حقل الدمج إلى عمود "القسم" في جدول البيانات. إذا كان هناك صف من هذا الجدول
// إذا كان لديه قيمة "HR" في عمود "القسم"، فسوف يلبي هذا الصف الشرط.
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "HR";

// أضف محتوى إلى مستندنا، وقم بإنشاء مصدر البيانات، ثم قم بتنفيذ دمج البريد.
builder.MoveToDocumentEnd();
builder.Write("Dear ");
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(", ");

 //يحتوي هذا الجدول على ثلاثة صفوف، وواحد منها يلبي شرط حقل SKIPIF الخاص بنا.
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

يوضح كيفية استخدام حقول MERGEREC وMERGESEQ لعدد وحساب سجلات دمج البريد في مستندات إخراج دمج البريد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(",");

// سيقوم حقل MERGEREC بطباعة رقم صف البيانات التي يتم دمجها في كل مستند إخراج دمج.
builder.Write("\nRow number of record in data source: ");
FieldMergeRec fieldMergeRec = (FieldMergeRec)builder.InsertField(FieldType.FieldMergeRec, true);

Assert.AreEqual(" MERGEREC ", fieldMergeRec.GetFieldCode());

// سيقوم حقل MERGESEQ بحساب عدد عمليات الدمج الناجحة وطباعة القيمة الحالية على كل صفحة على حدة.
// إذا لم يتخطى دمج البريد أي صفوف ولم يستدعي أي حقول SKIP/SKIPIF/NEXT/NEXTIF، فإن جميع عمليات الدمج تكون ناجحة.
// سوف تعرض الحقول MERGESEQ وMERGEREC نفس نتائج دمج البريد الناجح.
builder.Write("\nSuccessful merge number: ");
FieldMergeSeq fieldMergeSeq = (FieldMergeSeq)builder.InsertField(FieldType.FieldMergeSeq, true);

Assert.AreEqual(" MERGESEQ ", fieldMergeSeq.GetFieldCode());

// أدخل حقل SKIPIF، والذي سيقوم بتخطي الدمج إذا كان الاسم هو "John Doe".
FieldSkipIf fieldSkipIf = (FieldSkipIf)builder.InsertField(FieldType.FieldSkipIf, true);
builder.MoveTo(fieldSkipIf.Separator);
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "John Doe";

// قم بإنشاء مصدر بيانات يحتوي على 3 صفوف، بحيث يحتوي أحدها على "John Doe" كقيمة لعمود "الاسم".
// نظرًا لأن حقل SKIPIF سيتم تشغيله مرة واحدة بهذه القيمة، فإن إخراج دمج البريد الخاص بنا سيحتوي على صفحتين بدلاً من 3.
// في الصفحة 1، سيتم عرض "1" في الحقلين MERGESEQ وMERGEREC.
// في الصفحة 2، سيعرض حقل MERGEREC الرقم "3" وسيعرض حقل MERGESEQ الرقم "2".
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Rows.Add("Jane Doe");
table.Rows.Add("John Doe");
table.Rows.Add("Joe Bloggs");

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.MERGEREC.MERGESEQ.docx");
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
