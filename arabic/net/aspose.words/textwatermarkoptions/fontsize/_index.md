---
title: TextWatermarkOptions.FontSize
linktitle: FontSize
articleTitle: FontSize
second_title: Aspose.Words لـ .NET
description: خصّص خيارات علامة النص المائية لديك مع إمكانية تعديل حجم الخط. اضبط الحجم الذي يناسبك بسهولة لضمان وضوح وأسلوب مثاليين في تصميماتك.
type: docs
weight: 40
url: /ar/net/aspose.words/textwatermarkoptions/fontsize/
---
## TextWatermarkOptions.FontSize property

للحصول على حجم الخط أو تعيينه. القيمة الافتراضية هي 0 - تلقائي.

```csharp
public float FontSize { get; set; }
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentOutOfRangeException | يتم طرحه عندما تكون الحجة خارج نطاق القيم الصالحة. |

## ملاحظات

تتراوح القيم الصالحة من 0 إلى 65.5 شاملة.

يعني حجم الخط التلقائي أن العلامة المائية سيتم تغيير حجمها إلى أقصى عرض وأقصى ارتفاع بالنسبة إلى هوامش الصفحة.

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

* class [TextWatermarkOptions](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
