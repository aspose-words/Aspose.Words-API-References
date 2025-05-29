---
title: FieldMergeRec Class
linktitle: FieldMergeRec
articleTitle: FieldMergeRec
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.FieldMergeRec لدمج المستندات بسلاسة باستخدام حقل MERGEREC. حسّن أتمتة مستنداتك اليوم!
type: docs
weight: 2570
url: /ar/net/aspose.words.fields/fieldmergerec/
---
## FieldMergeRec class

ينفذ حقل MERGEREC.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldMergeRec : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldMergeRec](fieldmergerec/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/)الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | يحصل على أو يحدد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | يحصل على أو يحدد ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب نتيجته). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | يحصل على أو يعين LCID للحقل. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | يحصل على النص الموجود بين فاصل الحقل ونهاية الحقل أو يعينه. |
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

في الوقت الحالي، تنفذ حقول MERGEREC وMERGESEQ نفس الوظيفة لأننا لا نعرف على وجه اليقين كيفية تخطي السجلات في دمج البريد في Aspose.Words.

## أمثلة

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
