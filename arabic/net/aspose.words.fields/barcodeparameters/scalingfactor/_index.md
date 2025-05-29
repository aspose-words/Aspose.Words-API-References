---
title: BarcodeParameters.ScalingFactor
linktitle: ScalingFactor
articleTitle: ScalingFactor
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية BarcodeParameters ScalingFactor، التي تسمح بقياس دقيق للرمز في نقاط مئوية كاملة (10-1000) للحصول على أداء مثالي للرمز الشريطي.
type: docs
weight: 160
url: /ar/net/aspose.words.fields/barcodeparameters/scalingfactor/
---
## BarcodeParameters.ScalingFactor property

معامل القياس للرمز. القيمة بنقاط مئوية صحيحة، والقيم الصحيحة هي [10، 1000].

```csharp
public string ScalingFactor { get; set; }
```

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

* class [BarcodeParameters](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
