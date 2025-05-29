---
title: TextWatermarkOptions Class
linktitle: TextWatermarkOptions
articleTitle: TextWatermarkOptions
second_title: Aspose.Words لـ .NET
description: اكتشف خيارات Aspose.Words.TextWatermark للعلامات المائية النصية القابلة للتخصيص. حسّن مستنداتك بخيارات علامة تجارية فريدة واحترافية!
type: docs
weight: 7290
url: /ar/net/aspose.words/textwatermarkoptions/
---
## TextWatermarkOptions class

يحتوي على خيارات يمكن تحديدها عند إضافة علامة مائية مع نص.

لمعرفة المزيد، قم بزيارة[العمل مع العلامة المائية](https://docs.aspose.com/words/net/working-with-watermark/) مقالة توثيقية.

```csharp
public class TextWatermarkOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [TextWatermarkOptions](textwatermarkoptions/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Color](../../aspose.words/textwatermarkoptions/color/) { get; set; } | يُحدِّد لون الخط أو يُحدِّده. القيمة الافتراضية هيSilver . |
| [FontFamily](../../aspose.words/textwatermarkoptions/fontfamily/) { get; set; } | للحصول على اسم عائلة الخط أو تعيينه. القيمة الافتراضية هي "Calibri". |
| [FontSize](../../aspose.words/textwatermarkoptions/fontsize/) { get; set; } | للحصول على حجم الخط أو تعيينه. القيمة الافتراضية هي 0 - تلقائي. |
| [IsSemitrasparent](../../aspose.words/textwatermarkoptions/issemitrasparent/) { get; set; } | يحصل على قيمة منطقية أو يعينها وهي المسؤولة عن تعتيم العلامة المائية. القيمة الافتراضية هي`حقيقي` . |
| [Layout](../../aspose.words/textwatermarkoptions/layout/) { get; set; } | يُحدِّد أو يُحدِّد تخطيط العلامة المائية. القيمة الافتراضية هيDiagonal . |

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
