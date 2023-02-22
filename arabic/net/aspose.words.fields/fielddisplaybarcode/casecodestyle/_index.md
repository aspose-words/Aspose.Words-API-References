---
title: FieldDisplayBarcode.CaseCodeStyle
second_title: Aspose.Words لمراجع .NET API
description: FieldDisplayBarcode ملكية. الحصول على أو تحديد نمط رمز الحالة لنوع الرمز الشريطي ITF14. القيم الصالحة هي STD  EXT  ADD
type: docs
weight: 60
url: /ar/net/aspose.words.fields/fielddisplaybarcode/casecodestyle/
---
## FieldDisplayBarcode.CaseCodeStyle property

الحصول على أو تحديد نمط رمز الحالة لنوع الرمز الشريطي ITF14. القيم الصالحة هي [STD &#x7C; EXT &#x7C; ADD]

```csharp
public string CaseCodeStyle { get; set; }
```

### أمثلة

يوضح كيفية إدراج حقل DISPLAYBARCODE وتعيين خصائصه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDisplayBarcode field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);

// يوجد أدناه أربعة أنواع من الرموز الشريطية ، مزينة بطرق مختلفة ، والتي يمكن أن يعرضها حقل DISPLAYBARCODE.
// 1 - رمز الاستجابة السريعة بألوان مخصصة:
field.BarcodeType = "QR";
field.BarcodeValue = "ABC123";
field.BackgroundColor = "0xF8BD69";
field.ForegroundColor = "0xB5413B";
field.ErrorCorrectionLevel = "3";
field.ScalingFactor = "250";
field.SymbolHeight = "1000";
field.SymbolRotation = "0";

Assert.AreEqual(" DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0", field.GetFieldCode());
builder.Writeln();

// 2 - الباركود EAN13 ، مع عرض الأرقام أسفل الأشرطة:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "501234567890";
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// 3 - الرمز الشريطي CODE39:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "12345ABCDE";
field.AddStartStopChar = true;

Assert.AreEqual(" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// 4 - الباركود ITF4 ، مع رمز الحالة المحدد:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "09312345678907";
field.CaseCodeStyle = "STD";

Assert.AreEqual(" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.DISPLAYBARCODE.docx");
```

### أنظر أيضا

* class [FieldDisplayBarcode](../)
* مساحة الاسم [Aspose.Words.Fields](../../fielddisplaybarcode/)
* المجسم [Aspose.Words](../../../)


