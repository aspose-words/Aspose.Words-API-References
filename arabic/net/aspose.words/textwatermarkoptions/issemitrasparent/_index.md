---
title: TextWatermarkOptions.IsSemitrasparent
linktitle: IsSemitrasparent
articleTitle: IsSemitrasparent
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية TextWatermarkOptions IsSemitransparent - تحكم في شفافية العلامة المائية بسهولة. حسّن تصاميمك بإعدادات شفافية قابلة للتخصيص!
type: docs
weight: 50
url: /ar/net/aspose.words/textwatermarkoptions/issemitrasparent/
---
## TextWatermarkOptions.IsSemitrasparent property

يحصل على قيمة منطقية أو يعينها وهي المسؤولة عن تعتيم العلامة المائية. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool IsSemitrasparent { get; set; }
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

* class [TextWatermarkOptions](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
