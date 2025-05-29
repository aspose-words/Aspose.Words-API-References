---
title: FieldSkipIf.ComparisonOperator
linktitle: ComparisonOperator
articleTitle: ComparisonOperator
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldSkipIf ComparisonOperator، وقم بإدارة وتخصيص عوامل المقارنة الخاصة بك بسهولة لتحسين التعامل مع البيانات.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldskipif/comparisonoperator/
---
## FieldSkipIf.ComparisonOperator property

يحصل على عامل المقارنة أو يعينه.

```csharp
public string ComparisonOperator { get; set; }
```

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

* class [FieldSkipIf](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
