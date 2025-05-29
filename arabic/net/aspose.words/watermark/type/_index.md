---
title: Watermark.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية نوع العلامة المائية لتحسين تصميمك بعلامات مائية قابلة للتخصيص للعلامة التجارية والحماية. ارتقِ بمرئياتك اليوم!
type: docs
weight: 10
url: /ar/net/aspose.words/watermark/type/
---
## Watermark.Type property

يحصل على نوع العلامة المائية.

```csharp
public WatermarkType Type { get; }
```

## أمثلة

يوضح كيفية إنشاء علامة مائية نصية.

```csharp
Document doc = new Document();

//أضف علامة مائية نصية عادية.
doc.Watermark.SetText("Aspose Watermark");

// إذا أردنا تحرير تنسيق النص باستخدامه كعلامة مائية،
// يمكننا القيام بذلك عن طريق تمرير كائن TextWatermarkOptions عند إنشاء العلامة المائية.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

//يمكننا إزالة العلامة المائية من مستند مثل هذا.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### أنظر أيضا

* enum [WatermarkType](../../watermarktype/)
* class [Watermark](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
