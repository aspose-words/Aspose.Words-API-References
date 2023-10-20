---
title: BarcodeParameters.CaseCodeStyle
linktitle: CaseCodeStyle
articleTitle: CaseCodeStyle
second_title: Aspose.Words لـ .NET
description: BarcodeParameters CaseCodeStyle ملكية. نمط رمز الحالة لنوع الباركود ITF14. القيم الصالحة هي STDEXTADD في C#.
type: docs
weight: 60
url: /ar/net/aspose.words.fields/barcodeparameters/casecodestyle/
---
## BarcodeParameters.CaseCodeStyle property

نمط رمز الحالة لنوع الباركود ITF14. القيم الصالحة هي [STD&#x7C;EXT&#x7C;ADD]

```csharp
public string CaseCodeStyle { get; set; }
```

## أمثلة

يوضح كيفية استخدام مولد الباركود.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// يمكننا استخدام تطبيق IBarcodeGenerator مخصص لإنشاء الرموز الشريطية،
// ثم قم بإدراجها في المستند كصور.
doc.FieldOptions.BarcodeGenerator = new CustomBarcodeGenerator();

// فيما يلي أربعة أمثلة لأنواع مختلفة من الباركود التي يمكننا إنشاؤها باستخدام المولد الخاص بنا.
// لكل رمز شريطي، نحدد مجموعة جديدة من معلمات الرمز الشريطي، ثم نقوم بإنشاء الصورة.
// بعد ذلك، يمكننا إدراج الصورة في المستند، أو حفظها في نظام الملفات المحلي.
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

// 2 - الرمز الشريطي EAN13:
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

* class [BarcodeParameters](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
