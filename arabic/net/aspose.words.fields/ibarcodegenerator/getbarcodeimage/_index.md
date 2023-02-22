---
title: IBarcodeGenerator.GetBarcodeImage
second_title: Aspose.Words لمراجع .NET API
description: IBarcodeGenerator طريقة. إنشاء صورة الرمز الشريطي باستخدام مجموعة المعلمات لحقل DisplayBarcode .
type: docs
weight: 10
url: /ar/net/aspose.words.fields/ibarcodegenerator/getbarcodeimage/
---
## IBarcodeGenerator.GetBarcodeImage method

إنشاء صورة الرمز الشريطي باستخدام مجموعة المعلمات (لحقل DisplayBarcode) .

```csharp
public Image GetBarcodeImage(BarcodeParameters parameters)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| parameters | BarcodeParameters | مجموعة المعلمات |

### قيمة الإرجاع

صورة تمثل الرمز الشريطي الذي تم إنشاؤه.

### أمثلة

يوضح كيفية استخدام منشئ الباركود.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يمكننا استخدام تطبيق IBarcodeGenerator المخصص لإنشاء رموز شريطية ،
// ثم أدخلها في المستند كصور.
doc.FieldOptions.BarcodeGenerator = new CustomBarcodeGenerator();

// فيما يلي أربعة أمثلة لأنواع مختلفة من الرموز الشريطية التي يمكننا إنشاؤها باستخدام المولد الخاص بنا.
// لكل رمز شريطي ، نحدد مجموعة جديدة من معلمات الباركود ، ثم ننشئ الصورة.
// بعد ذلك ، يمكننا إدخال الصورة في المستند ، أو حفظها في نظام الملفات المحلي.
// 1 - رمز الاستجابة السريعة:
BarcodeParameters barcodeParameters = new BarcodeParameters
{
    BarcodeType = "QR",
    BarcodeValue = "ABC123",
    BackgroundColor = "0xF8BD69",
    ForegroundColor = "0xB5413B",
    ErrorCorrectionLevel = "3",
    ScalingFactor = "250",
    SymbolHeight = "1000",
    SymbolRotation = "0"
};

Image img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.QR.jpg");

builder.InsertImage(img);

// 2 - الباركود EAN13:
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "EAN13",
    BarcodeValue = "501234567890",
    DisplayText = true,
    PosCodeStyle = "CASE",
    FixCheckDigit = true
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.EAN13.jpg");
builder.InsertImage(img);

// 3 - الرمز الشريطي CODE39:
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "CODE39",
    BarcodeValue = "12345ABCDE",
    AddStartStopChar = true
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.CODE39.jpg");
builder.InsertImage(img);

// 4 - الباركود ITF14:
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "ITF14",
    BarcodeValue = "09312345678907",
    CaseCodeStyle = "STD"
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.ITF14.jpg");
builder.InsertImage(img);

doc.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.docx");
```

### أنظر أيضا

* class [BarcodeParameters](../../barcodeparameters/)
* interface [IBarcodeGenerator](../)
* مساحة الاسم [Aspose.Words.Fields](../../ibarcodegenerator/)
* المجسم [Aspose.Words](../../../)


