---
title: FieldMergeBarcode.AddStartStopChar
linktitle: AddStartStopChar
articleTitle: AddStartStopChar
second_title: Aspose.Words لـ .NET
description: FieldMergeBarcode AddStartStopChar ملكية. الحصول على أو تعيين ما إذا كان سيتم إضافة أحرف البدء/الإيقاف لأنواع الرموز الشريطية NW7 وCODE39 في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldmergebarcode/addstartstopchar/
---
## FieldMergeBarcode.AddStartStopChar property

الحصول على أو تعيين ما إذا كان سيتم إضافة أحرف البدء/الإيقاف لأنواع الرموز الشريطية NW7 وCODE39.

```csharp
public bool AddStartStopChar { get; set; }
```

## أمثلة

يوضح كيفية إجراء دمج البريد على الرموز الشريطية CODE39.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقل MERGEBARCODE، الذي سيقبل القيم من مصدر البيانات أثناء دمج البريد.
// سيقوم هذا الحقل بتحويل كافة القيم الموجودة في عمود "MyCODE39Barcode" الخاص بمصدر بيانات الدمج إلى رموز شريطية CODE39.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "MyCODE39Barcode";

// قم بتحرير مظهره لعرض أحرف البداية/الإيقاف.
field.AddStartStopChar = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyCODE39Barcode CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// قم بإنشاء DataTable بعمود يحمل نفس اسم قيمة BarcodeValue لحقل MERGEBARCODE الخاص بنا.
// سيؤدي دمج البريد إلى إنشاء صفحة جديدة لكل صف. ستحتوي كل صفحة على حقل DISPLAYBARCODE،
// والذي سيعرض الرمز الشريطي CODE39 بالقيمة من الصف المدمج.
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
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
