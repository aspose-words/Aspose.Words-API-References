---
title: WatermarkerContext.ImageWatermark
linktitle: ImageWatermark
articleTitle: ImageWatermark
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية تحسين صورك باستخدام خاصية Watermark ImageWatermark في WatermarkContext، مما يسمح لك بإضافة صور علامة مائية مخصصة بسهولة.
type: docs
weight: 20
url: /ar/net/aspose.words.lowcode/watermarkercontext/imagewatermark/
---
## WatermarkerContext.ImageWatermark property

بايتات الصورة المراد استخدامها كعلامة مائية.

```csharp
public byte[] ImageWatermark { get; set; }
```

## ملاحظات

إذا كان كلاهما`ImageWatermark` و[`TextWatermark`](../textwatermark/) يتم تحديد ذلك، حيث تتغلب العلامة المائية النصية على العلامة المائية للصورة.

## أمثلة

يوضح كيفية إدراج صورة العلامة المائية في المستند باستخدام السياق.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

WatermarkerContext watermarkerContext = new WatermarkerContext();
watermarkerContext.ImageWatermark = File.ReadAllBytes(watermarkImage);

watermarkerContext.ImageWatermarkOptions.Scale = 50;

Watermarker.Create(watermarkerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.WatermarkContextImage.docx")
    .Execute();
```

يوضح كيفية إدراج صورة العلامة المائية في المستند من مجرى باستخدام السياق.

```csharp
string watermarkImage = ImageDir + "Logo.jpg";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    WatermarkerContext watermarkerContext = new WatermarkerContext();
    watermarkerContext.ImageWatermark = File.ReadAllBytes(watermarkImage);

    watermarkerContext.ImageWatermarkOptions.Scale = 50;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkContextImageStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.Create(watermarkerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### أنظر أيضا

* class [WatermarkerContext](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
