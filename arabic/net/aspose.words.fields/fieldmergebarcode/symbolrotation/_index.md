---
title: FieldMergeBarcode.SymbolRotation
second_title: Aspose.Words لمراجع .NET API
description: FieldMergeBarcode ملكية. الحصول على أو تعيين تدوير رمز الباركود. القيم الصالحة هي 0  3
type: docs
weight: 140
url: /ar/net/aspose.words.fields/fieldmergebarcode/symbolrotation/
---
## FieldMergeBarcode.SymbolRotation property

الحصول على أو تعيين تدوير رمز الباركود. القيم الصالحة هي [0 ، 3]

```csharp
public string SymbolRotation { get; set; }
```

### أمثلة

يوضح كيفية إجراء دمج المراسلات على رموز QR الشريطية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقل MERGEBARCODE ، والذي سيقبل القيم من مصدر البيانات أثناء دمج البريد.
// سيحول هذا الحقل جميع القيم الموجودة في عمود "MyQRCode" الخاص بمصدر بيانات الدمج إلى أكواد QR.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "QR";
field.BarcodeValue = "MyQRCode";

// تطبيق ألوان وقياسات مخصصة.
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

// قم بإنشاء DataTable بعمود بنفس الاسم مثل BarcodeValue الخاص بحقل MERGEBARCODE.
// سيقوم دمج البريد بإنشاء صفحة جديدة لكل صف. ستحتوي كل صفحة على حقل DISPLAYBARCODE ،
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
* مساحة الاسم [Aspose.Words.Fields](../../fieldmergebarcode/)
* المجسم [Aspose.Words](../../../)


