---
title: WatermarkerContext.TextWatermark
linktitle: TextWatermark
articleTitle: TextWatermark
second_title: Aspose.Words لـ .NET
description: اكتشف ميزة Watermark TextWatermark في WatermarkContext لإضافة علامات مائية نصية قابلة للتخصيص بسهولة، مما يعزز أمان المحتوى الخاص بك وعلامتك التجارية.
type: docs
weight: 40
url: /ar/net/aspose.words.lowcode/watermarkercontext/textwatermark/
---
## WatermarkerContext.TextWatermark property

النص الذي سيتم استخدامه كعلامة مائية.

```csharp
public string TextWatermark { get; set; }
```

## ملاحظات

إذا كان كلاهما[`ImageWatermark`](../imagewatermark/) و`TextWatermark` يتم تحديد ذلك، حيث تتغلب العلامة المائية النصية على العلامة المائية للصورة.

## أمثلة

يوضح كيفية إدراج نص العلامة المائية في المستند باستخدام السياق.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

WatermarkerContext watermarkerContext = new WatermarkerContext();
watermarkerContext.TextWatermark = watermarkText;

watermarkerContext.TextWatermarkOptions.Color = Color.Red;

Watermarker.Create(watermarkerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.WatermarkContextText.docx")
    .Execute();
```

يوضح كيفية إدراج نص العلامة المائية في المستند من التدفق باستخدام السياق.

```csharp
string watermarkText = "This is a watermark";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    WatermarkerContext watermarkerContext = new WatermarkerContext();
    watermarkerContext.TextWatermark = watermarkText;

    watermarkerContext.TextWatermarkOptions.Color = Color.Red;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkContextTextStream.docx", FileMode.Create, FileAccess.ReadWrite))
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
