---
title: FieldMergeBarcode.SymbolHeight
linktitle: SymbolHeight
articleTitle: SymbolHeight
second_title: Aspose.Words لـ .NET
description: اضبط خاصية FieldMergeBarcode SymbolHeight لتخصيص ارتفاع الباركود الخاص بك بوحدات TWIPS. حسّن عرض بياناتك بدقة!
type: docs
weight: 130
url: /ar/net/aspose.words.fields/fieldmergebarcode/symbolheight/
---
## FieldMergeBarcode.SymbolHeight property

يُحدِّد ارتفاع الرمز أو يُحدِّده. الوحدات بوحدة TWIPS (1/1440 بوصة).

```csharp
public string SymbolHeight { get; set; }
```

## أمثلة

يوضح كيفية تنفيذ عملية دمج البريد على رموز QR.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقل MERGEBARCODE، الذي سيقبل القيم من مصدر البيانات أثناء دمج البريد.
// سيقوم هذا الحقل بتحويل جميع القيم الموجودة في عمود "MyQRCode" الخاص بمصدر بيانات الدمج إلى رموز QR.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "QR";
field.BarcodeValue = "MyQRCode";

// تطبيق الألوان المخصصة والتدرج.
field.BackgroundColor = "0xF8BD69";
field.ForegroundColor = "0xB5413B";
field.ErrorCorrectionLevel = "3";
field.ScalingFactor = "250";
field.SymbolHeight = "1000";
field.SymbolRotation = "0";

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyQRCode QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0",
    field.GetFieldCode());
builder.Writeln();

// قم بإنشاء جدول بيانات بعمود يحمل نفس اسم BarcodeValue الخاص بحقل MERGEBARCODE.
// سيؤدي دمج البريد إلى إنشاء صفحة جديدة لكل صف. ستحتوي كل صفحة على حقل DISPLAYBARCODE.
// الذي سيعرض رمز الاستجابة السريعة بالقيمة من الصف المدمج.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyQRCode");
table.Rows.Add(new[] { "ABC123" });
table.Rows.Add(new[] { "DEF456" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"ABC123\" QR \\q 3 \\s 250 \\h 1000 \\r 0 \\b 0xF8BD69 \\f 0xB5413B", 
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"DEF456\" QR \\q 3 \\s 250 \\h 1000 \\r 0 \\b 0xF8BD69 \\f 0xB5413B",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.QR.docx");
```

### أنظر أيضا

* class [FieldMergeBarcode](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
