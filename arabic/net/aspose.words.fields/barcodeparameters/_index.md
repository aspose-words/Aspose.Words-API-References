---
title: BarcodeParameters Class
linktitle: BarcodeParameters
articleTitle: BarcodeParameters
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.BarcodeParameters—أداة أساسية لإنشاء الباركود وتخصيصه بسلاسة في معالجة المستندات.
type: docs
weight: 1880
url: /ar/net/aspose.words.fields/barcodeparameters/
---
## BarcodeParameters class

فئة الحاوية لمعلمات الباركود التي سيتم تمريرها إلى BarcodeGenerator.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

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
| [AddStartStopChar](../../aspose.words.fields/barcodeparameters/addstartstopchar/) { get; set; } | ما إذا كان سيتم إضافة أحرف البدء/الإيقاف لأنواع الباركود NW7 وCODE39. |
| [BackgroundColor](../../aspose.words.fields/barcodeparameters/backgroundcolor/) { get; set; } | لون خلفية الرمز الشريطي (0x000000 - 0xFFFFFF) |
| [BarcodeType](../../aspose.words.fields/barcodeparameters/barcodetype/) { get; set; } | نوع الرمز الشريطي. |
| [BarcodeValue](../../aspose.words.fields/barcodeparameters/barcodevalue/) { get; set; } | البيانات المراد ترميزها. |
| [CaseCodeStyle](../../aspose.words.fields/barcodeparameters/casecodestyle/) { get; set; } | نمط رمز الحالة لنوع الباركود ITF14. القيم الصحيحة هي [STD&#x7C;EXT&#x7C;ADD] |
| [DisplayText](../../aspose.words.fields/barcodeparameters/displaytext/) { get; set; } | ما إذا كان سيتم عرض بيانات الباركود (النص) مع الصورة. |
| [ErrorCorrectionLevel](../../aspose.words.fields/barcodeparameters/errorcorrectionlevel/) { get; set; } | مستوى تصحيح خطأ رمز الاستجابة السريعة (QR Code) هو [0، 3]. |
| [FacingIdentificationMark](../../aspose.words.fields/barcodeparameters/facingidentificationmark/) { get; set; } | نوع علامة التعريف المواجهة (FIM). |
| [FixCheckDigit](../../aspose.words.fields/barcodeparameters/fixcheckdigit/) { get; set; } | ما إذا كان سيتم إصلاح رقم الفحص إذا كان غير صالح. |
| [ForegroundColor](../../aspose.words.fields/barcodeparameters/foregroundcolor/) { get; set; } | لون مقدمة الرمز الشريطي (0x000000 - 0xFFFFFF) |
| [IsBookmark](../../aspose.words.fields/barcodeparameters/isbookmark/) { get; set; } | سواء[`PostalAddress`](./postaladdress/) هو اسم الإشارة المرجعية. |
| [IsUSPostalAddress](../../aspose.words.fields/barcodeparameters/isuspostaladdress/) { get; set; } | سواء[`PostalAddress`](./postaladdress/) هو عنوان بريدي أمريكي. |
| [PosCodeStyle](../../aspose.words.fields/barcodeparameters/poscodestyle/) { get; set; } | نمط رمز نقطة البيع (أنواع الباركود: UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). القيم الصحيحة (غير حساسة لحالة الأحرف) هي [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE]. |
| [PostalAddress](../../aspose.words.fields/barcodeparameters/postaladdress/) { get; set; } | عنوان البريد الإلكتروني بالباركود. |
| [ScalingFactor](../../aspose.words.fields/barcodeparameters/scalingfactor/) { get; set; } | معامل القياس للرمز. القيمة بنقاط مئوية صحيحة، والقيم الصحيحة هي [10، 1000]. |
| [SymbolHeight](../../aspose.words.fields/barcodeparameters/symbolheight/) { get; set; } | ارتفاع صورة الرمز الشريطي (بالتويب - 1/1440 بوصة) |
| [SymbolRotation](../../aspose.words.fields/barcodeparameters/symbolrotation/) { get; set; } | تدوير رمز الباركود. القيم الصحيحة هي [0، 3]. |

## ملاحظات

مجموعة المعلمات وفقًا لخيارات حقل DISPLAYBARCODE. راجع القائمة الدقيقة في[https://msdn.microsoft.com/en-us/library/hh745901(v=office.12).aspx](https://msdn.microsoft.com/en-us/library/hh745901(v=office.12).aspx)

## أمثلة

يوضح كيفية استخدام مولد الباركود.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// يمكننا استخدام تنفيذ IBarcodeGenerator مخصص لتوليد الرموز الشريطية،
//ثم قم بإدراجها في المستند كصور.
doc.FieldOptions.BarcodeGenerator = new CustomBarcodeGenerator();

// فيما يلي أربعة أمثلة لأنواع مختلفة من الرموز الشريطية التي يمكننا إنشاؤها باستخدام المولد الخاص بنا.
// بالنسبة لكل رمز شريطي، نحدد مجموعة جديدة من معلمات الرمز الشريطي، ثم نقوم بإنشاء الصورة.
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
#if NET461_OR_GREATER || JAVA
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.QR.jpg");
#elif NET5_0_OR_GREATER
using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "FieldOptions.BarcodeGenerator.QR.jpg"))
{
    img.Encode(fs, SKEncodedImageFormat.Jpeg, 100);
}
#endif
builder.InsertImage(img);

// 2 - رمز الباركود EAN13:
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "EAN13",
    BarcodeValue = "501234567890",
    DisplayText = true,
    PosCodeStyle = "CASE",
    FixCheckDigit = true
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
#if NET461_OR_GREATER || JAVA
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.EAN13.jpg");
#elif NET5_0_OR_GREATER
using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "FieldOptions.BarcodeGenerator.EAN13.jpg"))
{
    img.Encode(fs, SKEncodedImageFormat.Jpeg, 100);
}
#endif
builder.InsertImage(img);

// 3 - الرمز الشريطي CODE39:
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "CODE39",
    BarcodeValue = "12345ABCDE",
    AddStartStopChar = true
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
#if NET461_OR_GREATER || JAVA
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.CODE39.jpg");
#elif NET5_0_OR_GREATER
using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "FieldOptions.BarcodeGenerator.CODE39.jpg"))
{
    img.Encode(fs, SKEncodedImageFormat.Jpeg, 100);
}
#endif
builder.InsertImage(img);

// 4 - رمز الباركود ITF14:
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "ITF14",
    BarcodeValue = "09312345678907",
    CaseCodeStyle = "STD"
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
#if NET461_OR_GREATER || JAVA
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.ITF14.jpg");
#elif NET5_0_OR_GREATER
using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "FieldOptions.BarcodeGenerator.ITF14.jpg"))
{
    img.Encode(fs, SKEncodedImageFormat.Jpeg, 100);
}
#endif
builder.InsertImage(img);

doc.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
