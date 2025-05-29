---
title: TextWatermarkOptions.Layout
linktitle: Layout
articleTitle: Layout
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية تخطيط TextWatermarkOptions لتخصيص مظهر علامتك المائية. اضبطها بسهولة على "قطري" أو التخطيط المفضل لديك لتحسين المظهر المرئي.
type: docs
weight: 60
url: /ar/net/aspose.words/textwatermarkoptions/layout/
---
## TextWatermarkOptions.Layout property

يُحدِّد أو يُحدِّد تخطيط العلامة المائية. القيمة الافتراضية هيDiagonal .

```csharp
public WatermarkLayout Layout { get; set; }
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

* enum [WatermarkLayout](../../watermarklayout/)
* class [TextWatermarkOptions](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
