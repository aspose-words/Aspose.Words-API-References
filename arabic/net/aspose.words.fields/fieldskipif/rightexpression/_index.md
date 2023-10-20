---
title: FieldSkipIf.RightExpression
linktitle: RightExpression
articleTitle: RightExpression
second_title: Aspose.Words لـ .NET
description: FieldSkipIf RightExpression ملكية. الحصول على أو تعيين الجزء الأيمن من تعبير المقارنة في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.fields/fieldskipif/rightexpression/
---
## FieldSkipIf.RightExpression property

الحصول على أو تعيين الجزء الأيمن من تعبير المقارنة.

```csharp
public string RightExpression { get; set; }
```

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

* class [FieldSkipIf](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
