---
title: TextWatermarkOptions.FontSize
second_title: Aspose.Words لمراجع .NET API
description: TextWatermarkOptions ملكية. الحصول على حجم الخط أو تحديده. القيمة الافتراضية هي 0  auto .
type: docs
weight: 40
url: /ar/net/aspose.words/textwatermarkoptions/fontsize/
---
## TextWatermarkOptions.FontSize property

الحصول على حجم الخط أو تحديده. القيمة الافتراضية هي 0 - auto .

```csharp
public float FontSize { get; set; }
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentOutOfRangeException | يظهر عندما تكون الوسيطة خارج نطاق القيم الصالحة. |

### ملاحظات

تتراوح القيم الصالحة من 0 إلى 65.5 ضمناً.

يعني حجم الخط التلقائي أنه سيتم تغيير حجم العلامة المائية إلى أقصى عرض لها وأقصى ارتفاع لها بالنسبة إلى هوامش الصفحة.

### أمثلة

يوضح كيفية إنشاء علامة مائية نصية.

```csharp
Document doc = new Document();

// أضف علامة مائية بنص عادي.
doc.Watermark.SetText("Aspose Watermark");

// إذا كنا نرغب في تحرير تنسيق النص باستخدامه كعلامة مائية ،
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


