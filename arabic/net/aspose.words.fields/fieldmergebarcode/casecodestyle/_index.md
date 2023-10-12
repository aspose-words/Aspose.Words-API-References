---
title: FieldMergeBarcode.CaseCodeStyle
second_title: Aspose.Words لمراجع .NET API
description: FieldMergeBarcode ملكية. الحصول على أو تعيين نمط رمز الحالة لنوع الرمز الشريطي ITF14. القيم الصالحة هي STDEXTADD
type: docs
weight: 60
url: /ar/net/aspose.words.fields/fieldmergebarcode/casecodestyle/
---
## FieldMergeBarcode.CaseCodeStyle property

الحصول على أو تعيين نمط رمز الحالة لنوع الرمز الشريطي ITF14. القيم الصالحة هي [STD&#x7C;EXT&#x7C;ADD]

```csharp
public string CaseCodeStyle { get; set; }
```

### أمثلة

يوضح كيفية إجراء دمج البريد على الرموز الشريطية ITF14.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقل MERGEBARCODE، الذي سيقبل القيم من مصدر البيانات أثناء دمج البريد.
// سيقوم هذا الحقل بتحويل كافة القيم الموجودة في عمود "MyITF14Barcode" الخاص بمصدر بيانات الدمج إلى رموز شريطية ITF14.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "MyITF14Barcode";
field.CaseCodeStyle = "STD";

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyITF14Barcode ITF14 \\c STD", field.GetFieldCode());

// قم بإنشاء DataTable بعمود يحمل نفس اسم قيمة BarcodeValue لحقل MERGEBARCODE الخاص بنا.
// سيؤدي دمج البريد إلى إنشاء صفحة جديدة لكل صف. ستحتوي كل صفحة على حقل DISPLAYBARCODE،
// والذي سيعرض الرمز الشريطي ITF14 بالقيمة من الصف المدمج.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyITF14Barcode");
table.Rows.Add(new[] { "09312345678907" });
table.Rows.Add(new[] { "1234567891234" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"09312345678907\" ITF14 \\c STD",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"1234567891234\" ITF14 \\c STD",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.ITF14.docx");
```

### أنظر أيضا

* class [FieldMergeBarcode](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldmergebarcode/)
* المجسم [Aspose.Words](../../../)


