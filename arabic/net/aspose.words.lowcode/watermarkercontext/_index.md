---
title: WatermarkerContext Class
linktitle: WatermarkerContext
articleTitle: WatermarkerContext
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.LowCode.WatermarkerContext لإضافة علامات مائية سلسة إلى مستنداتك. حسّن مستنداتك بسهولة وكفاءة.
type: docs
weight: 4450
url: /ar/net/aspose.words.lowcode/watermarkercontext/
---
## WatermarkerContext class

سياق العلامة المائية للمستند.

```csharp
public class WatermarkerContext : ProcessorContext
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [WatermarkerContext](watermarkercontext/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | إعدادات الخط المستخدمة بواسطة المعالج. |
| [ImageWatermark](../../aspose.words.lowcode/watermarkercontext/imagewatermark/) { get; set; } | بايتات الصورة المراد استخدامها كعلامة مائية. |
| [ImageWatermarkOptions](../../aspose.words.lowcode/watermarkercontext/imagewatermarkoptions/) { get; } | خيارات العلامة المائية النصية. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | خيارات تخطيط المستند التي يستخدمها المعالج. |
| [TextWatermark](../../aspose.words.lowcode/watermarkercontext/textwatermark/) { get; set; } | النص الذي سيتم استخدامه كعلامة مائية. |
| [TextWatermarkOptions](../../aspose.words.lowcode/watermarkercontext/textwatermarkoptions/) { get; } | خيارات العلامة المائية للصورة. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | استدعاء تحذيري يستخدمه المعالج. |

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

* class [ProcessorContext](../processorcontext/)
* مساحة الاسم [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../)
