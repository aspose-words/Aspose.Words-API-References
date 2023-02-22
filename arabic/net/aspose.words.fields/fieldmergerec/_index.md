---
title: Class FieldMergeRec
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.FieldMergeRec فصل. تنفذ حقل MERGEREC .
type: docs
weight: 2010
url: /ar/net/aspose.words.fields/fieldmergerec/
---
## FieldMergeRec class

تنفذ حقل MERGEREC .

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
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على أ[`FieldFormat`](../fieldformat/) كائن يوفر وصولاً مكتوبًا إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | تحديد ما إذا كان الحقل مغلقًا أم لا (يجب عدم إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تحديد LCID للحقل. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل المجال. يمكن أن يكون فارغًا. |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | يحصل على نوع حقل Microsoft Word . |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . |
| [Remove](../../aspose.words.fields/field/remove/)() | يزيل الحقل من المستند. إرجاع عقدة بعد الحقل مباشرة. إذا كانت نهاية الحقل هي آخر child من العقدة الأصلية ، يتم إرجاع فقرته الأصلية. إذا تمت إزالة الحقل بالفعل ، يعود **لا شيء** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يقوم بالتحديث الميداني. يرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(bool) | يقوم بإجراء تحديث ميداني. يرمي إذا تم تحديث الحقل بالفعل. |

### ملاحظات

في الوقت الحالي ، يقوم حقلا MERGEREC و MERGESEQ بتنفيذ نفس الوظيفة لأننا لا نعرف على وجه اليقين كيفية تخطي السجلات في Aspose.Words دمج المراسلات.

### أمثلة

يوضح كيفية استخدام حقلي MERGEREC و MERGESEQ للرقم وإحصاء سجلات دمج المراسلات في مستندات الإخراج لدمج المراسلات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(",");

// سيطبع حقل MERGEREC رقم صف البيانات التي يتم دمجها في كل مستند إخراج دمج.
builder.Write("\nRow number of record in data source: ");
FieldMergeRec fieldMergeRec = (FieldMergeRec)builder.InsertField(FieldType.FieldMergeRec, true);

Assert.AreEqual(" MERGEREC ", fieldMergeRec.GetFieldCode());

// سيحسب حقل MERGESEQ عدد عمليات الدمج الناجحة ويطبع القيمة الحالية في كل صفحة على حدة.
// إذا لم يتخطى دمج المراسلات أي صفوف ولم يستدعي حقول SKIP / SKIPIF / NEXT / NEXTIF ، فإن جميع عمليات الدمج تكون ناجحة.
// سيعرض حقلا MERGESEQ و MERGEREC نفس نتائج دمج البريد بنجاح.
builder.Write("\nSuccessful merge number: ");
FieldMergeSeq fieldMergeSeq = (FieldMergeSeq)builder.InsertField(FieldType.FieldMergeSeq, true);

Assert.AreEqual(" MERGESEQ ", fieldMergeSeq.GetFieldCode());

// أدخل حقل SKIPIF ، والذي سيتخطى الدمج إذا كان الاسم هو "John Doe".
FieldSkipIf fieldSkipIf = (FieldSkipIf)builder.InsertField(FieldType.FieldSkipIf, true);
builder.MoveTo(fieldSkipIf.Separator);
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "John Doe";

// أنشئ مصدر بيانات بثلاثة صفوف ، يحتوي أحدها على "John Doe" كقيمة لعمود "الاسم".
// نظرًا لأنه سيتم تشغيل حقل SKIPIF مرة واحدة بهذه القيمة ، فسيكون ناتج دمج البريد الخاص بنا عبارة عن صفحتين بدلاً من 3.
// في الصفحة 1 ، سيعرض كل من حقلي MERGESEQ و MERGEREC الرقم "1".
// في الصفحة 2 ، سيعرض حقل MERGEREC "3" وسيعرض حقل MERGESEQ "2".
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


