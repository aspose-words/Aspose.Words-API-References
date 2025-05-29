---
title: FieldMergeBarcode.FixCheckDigit
linktitle: FixCheckDigit
articleTitle: FixCheckDigit
second_title: Aspose.Words لـ .NET
description: قم بتحسين FieldMergeBarcode الخاص بك باستخدام خاصية FixCheckDigit لضمان التحقق الدقيق من رقم التحقق وتعزيز سلامة البيانات دون عناء.
type: docs
weight: 90
url: /ar/net/aspose.words.fields/fieldmergebarcode/fixcheckdigit/
---
## FieldMergeBarcode.FixCheckDigit property

يحصل على أو يحدد ما إذا كان سيتم إصلاح رقم الاختبار إذا كان غير صالح.

```csharp
public bool FixCheckDigit { get; set; }
```

## أمثلة

يوضح كيفية تنفيذ عملية دمج البريد على رموز الباركود EAN13.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقل MERGEBARCODE، الذي سيقبل القيم من مصدر البيانات أثناء دمج البريد.
// سيقوم هذا الحقل بتحويل جميع القيم الموجودة في عمود "MyEAN13Barcode" الخاص بمصدر بيانات الدمج إلى رموز شريطية EAN13.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "MyEAN13Barcode";

//عرض القيمة الرقمية للرمز الشريطي أسفل الأشرطة.
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// قم بإنشاء جدول بيانات بعمود يحمل نفس اسم BarcodeValue الخاص بحقل MERGEBARCODE.
// سيؤدي دمج البريد إلى إنشاء صفحة جديدة لكل صف. ستحتوي كل صفحة على حقل DISPLAYBARCODE.
// الذي سيعرض رمز شريطي EAN13 بالقيمة من الصف المدمج.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyEAN13Barcode");
table.Rows.Add(new[] { "501234567890" });
table.Rows.Add(new[] { "123456789012" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"501234567890\" EAN13 \\t \\p CASE \\x",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"123456789012\" EAN13 \\t \\p CASE \\x",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.EAN13.docx");
```

### أنظر أيضا

* class [FieldMergeBarcode](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
