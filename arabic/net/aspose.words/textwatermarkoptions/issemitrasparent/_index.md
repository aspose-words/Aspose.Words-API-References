---
title: TextWatermarkOptions.IsSemitrasparent
second_title: Aspose.Words لمراجع .NET API
description: TextWatermarkOptions ملكية. الحصول على أو تعيين قيمة منطقية مسؤولة عن عتامة العلامة المائية. القيمة الافتراضية هيحقيقي .
type: docs
weight: 50
url: /ar/net/aspose.words/textwatermarkoptions/issemitrasparent/
---
## TextWatermarkOptions.IsSemitrasparent property

الحصول على أو تعيين قيمة منطقية مسؤولة عن عتامة العلامة المائية. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool IsSemitrasparent { get; set; }
```

### أمثلة

يوضح كيفية إنشاء علامة مائية نصية.

```csharp
Document doc = new Document();

// أضف علامة مائية نصية عادية.
doc.Watermark.SetText("Aspose Watermark");

// إذا أردنا تعديل تنسيق النص باستخدامه كعلامة مائية،
// يمكننا القيام بذلك عن طريق تمرير كائن TextWatermarkOptions عند إنشاء العلامة المائية.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// يمكننا إزالة علامة مائية من مستند مثل هذا.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### أنظر أيضا

* class [TextWatermarkOptions](../)
* مساحة الاسم [Aspose.Words](../../textwatermarkoptions/)
* المجسم [Aspose.Words](../../../)


