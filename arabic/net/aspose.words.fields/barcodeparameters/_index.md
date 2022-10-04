---
title: BarcodeParameters
second_title: Aspose.Words لمراجع .NET API
description: فئة حاوية لمعلمات الباركود لتمريرها إلى BarcodeGenerator.
type: docs
weight: 1320
url: /ar/net/aspose.words.fields/barcodeparameters/
---
## BarcodeParameters class

فئة حاوية لمعلمات الباركود لتمريرها إلى BarcodeGenerator.

```csharp
public class BarcodeParameters
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [BarcodeParameters](barcodeparameters/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AddStartStopChar](../../aspose.words.fields/barcodeparameters/addstartstopchar/) { get; set; } | ما إذا كنت تريد إضافة أحرف بدء / إيقاف لأنواع الباركود NW7 و CODE39. |
| [BackgroundColor](../../aspose.words.fields/barcodeparameters/backgroundcolor/) { get; set; } | لون خلفية الرمز الشريطي (0x000000 - 0xFFFFFF) |
| [BarcodeType](../../aspose.words.fields/barcodeparameters/barcodetype/) { get; set; } | نوع الرمز الشريطي . |
| [BarcodeValue](../../aspose.words.fields/barcodeparameters/barcodevalue/) { get; set; } | البيانات المراد تشفيرها . |
| [CaseCodeStyle](../../aspose.words.fields/barcodeparameters/casecodestyle/) { get; set; } | نمط رمز الحالة لنوع الرمز الشريطي ITF14. القيم الصالحة هي [STD &#x7C; EXT &#x7C; ADD] |
| [DisplayText](../../aspose.words.fields/barcodeparameters/displaytext/) { get; set; } | عرض بيانات الباركود (نص) مع الصورة. |
| [ErrorCorrectionLevel](../../aspose.words.fields/barcodeparameters/errorcorrectionlevel/) { get; set; } | مستوى تصحيح الخطأ لرمز الاستجابة السريعة. القيم الصالحة هي [0 ، 3] . |
| [FacingIdentificationMark](../../aspose.words.fields/barcodeparameters/facingidentificationmark/) { get; set; } | نوع علامة تحديد الوجه (FIM) . |
| [FixCheckDigit](../../aspose.words.fields/barcodeparameters/fixcheckdigit/) { get; set; } | تحديد ما إذا كان يجب إصلاح خانة الاختيار إذا كانت غير صالحة. |
| [ForegroundColor](../../aspose.words.fields/barcodeparameters/foregroundcolor/) { get; set; } | لون مقدمة الرمز الشريطي (0x000000 - 0xFFFFFF) |
| [IsBookmark](../../aspose.words.fields/barcodeparameters/isbookmark/) { get; set; } | سواء[`PostalAddress`](./postaladdress/) هو اسم إشارة مرجعية . |
| [IsUSPostalAddress](../../aspose.words.fields/barcodeparameters/isuspostaladdress/) { get; set; } | سواء[`PostalAddress`](./postaladdress/) هو عنوان بريدي أمريكي. |
| [PosCodeStyle](../../aspose.words.fields/barcodeparameters/poscodestyle/) { get; set; } | نمط الرمز الشريطي لنقطة البيع (أنواع الرموز الشريطية UPCA &#x7C; UPCE &#x7C; EAN13 &#x7C; EAN8). القيم الصالحة (غير حساسة لحالة الأحرف) هي [STD &#x7C; SUP2 &#x7C; SUP5 &#x7C; CASE] . |
| [PostalAddress](../../aspose.words.fields/barcodeparameters/postaladdress/) { get; set; } | العنوان البريدي للرمز الشريطي . |
| [ScalingFactor](../../aspose.words.fields/barcodeparameters/scalingfactor/) { get; set; } | معامل القياس للرمز. القيمة بالنقاط المئوية الكاملة والقيم الصالحة هي [10 ، 1000] . |
| [SymbolHeight](../../aspose.words.fields/barcodeparameters/symbolheight/) { get; set; } | ارتفاع صورة الرمز الشريطي (بالتويب - 1/1440 بوصة) |
| [SymbolRotation](../../aspose.words.fields/barcodeparameters/symbolrotation/) { get; set; } | دوران رمز الباركود. القيم الصالحة هي [0 ، 3] . |

### ملاحظات

مجموعة المعلمات طبقًا لخيارات حقل DISPLAYBARCODE . انظر القائمة الدقيقة على[https://msdn.microsoft.com/en-us/library/hh745901(v=office.12).aspx](https://msdn.microsoft.com/en-us/library/hh745901(v=office.12).aspx)

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

* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
