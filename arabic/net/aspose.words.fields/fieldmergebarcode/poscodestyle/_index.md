---
title: FieldMergeBarcode.PosCodeStyle
second_title: Aspose.Words لمراجع .NET API
description: FieldMergeBarcode ملكية. الحصول على أو تعيين نمط الرمز الشريطي لنقطة البيع أنواع الرموز الشريطية UPCAUPCEEAN13EAN8. القيم الصالحة غير حساسة لحالة الأحرف هي STDSUP2SUP5CASE.
type: docs
weight: 110
url: /ar/net/aspose.words.fields/fieldmergebarcode/poscodestyle/
---
## FieldMergeBarcode.PosCodeStyle property

الحصول على أو تعيين نمط الرمز الشريطي لنقطة البيع (أنواع الرموز الشريطية UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). القيم الصالحة (غير حساسة لحالة الأحرف) هي [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE].

```csharp
public string PosCodeStyle { get; set; }
```

### أمثلة

يوضح كيفية إجراء دمج البريد على الرموز الشريطية EAN13.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقل MERGEBARCODE، الذي سيقبل القيم من مصدر البيانات أثناء دمج البريد.
// سيقوم هذا الحقل بتحويل كافة القيم الموجودة في عمود "MyEAN13Barcode" الخاص بمصدر بيانات الدمج إلى رموز شريطية EAN13.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "MyEAN13Barcode";

// عرض القيمة الرقمية للرمز الشريطي أسفل الأشرطة.
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// قم بإنشاء DataTable بعمود يحمل نفس اسم قيمة BarcodeValue لحقل MERGEBARCODE الخاص بنا.
// سيؤدي دمج البريد إلى إنشاء صفحة جديدة لكل صف. ستحتوي كل صفحة على حقل DISPLAYBARCODE،
// والذي سيعرض الرمز الشريطي EAN13 بالقيمة من الصف المدمج.
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
* مساحة الاسم [Aspose.Words.Fields](../../fieldmergebarcode/)
* المجسم [Aspose.Words](../../../)


