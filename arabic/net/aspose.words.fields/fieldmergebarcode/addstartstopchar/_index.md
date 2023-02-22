---
title: FieldMergeBarcode.AddStartStopChar
second_title: Aspose.Words لمراجع .NET API
description: FieldMergeBarcode ملكية. الحصول على أو تحديد ما إذا كان سيتم إضافة أحرف بدء / إيقاف لأنواع الباركود NW7 و CODE39.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldmergebarcode/addstartstopchar/
---
## FieldMergeBarcode.AddStartStopChar property

الحصول على أو تحديد ما إذا كان سيتم إضافة أحرف بدء / إيقاف لأنواع الباركود NW7 و CODE39.

```csharp
public bool AddStartStopChar { get; set; }
```

### أمثلة

يوضح كيفية تنفيذ دمج المراسلات على الرموز الشريطية CODE39.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقل MERGEBARCODE ، والذي سيقبل القيم من مصدر البيانات أثناء دمج البريد.
// سيقوم هذا الحقل بتحويل جميع القيم الموجودة في عمود "MyCODE39Barcode" الخاص بمصدر بيانات الدمج إلى الرموز الشريطية CODE39.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "MyCODE39Barcode";

// تحرير مظهره لعرض أحرف البداية / الإيقاف.
field.AddStartStopChar = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyCODE39Barcode CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// قم بإنشاء DataTable بعمود بنفس الاسم مثل BarcodeValue الخاص بحقل MERGEBARCODE.
// سيقوم دمج البريد بإنشاء صفحة جديدة لكل صف. ستحتوي كل صفحة على حقل DISPLAYBARCODE ،
// الذي سيعرض الرمز الشريطي CODE39 بالقيمة من الصف المدمج.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyCODE39Barcode");
table.Rows.Add(new[] { "12345ABCDE" });
table.Rows.Add(new[] { "67890FGHIJ" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"12345ABCDE\" CODE39 \\d",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"67890FGHIJ\" CODE39 \\d",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.CODE39.docx");
```

### أنظر أيضا

* class [FieldMergeBarcode](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldmergebarcode/)
* المجسم [Aspose.Words](../../../)


