---
title: Watermark Class
linktitle: Watermark
articleTitle: Watermark
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Watermark لإضافة العلامات المائية وتخصيصها بسهولة في مستنداتك، مما يعزز الاحترافية والعلامة التجارية.
type: docs
weight: 7520
url: /ar/net/aspose.words/watermark/
---
## Watermark class

يمثل الفئة التي سيتم العمل بها مع العلامة المائية للمستند.

لمعرفة المزيد، قم بزيارة[العمل مع العلامة المائية](https://docs.aspose.com/words/net/working-with-watermark/) مقالة توثيقية.

```csharp
public sealed class Watermark
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Type](../../aspose.words/watermark/type/) { get; } | يحصل على نوع العلامة المائية. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Remove](../../aspose.words/watermark/remove/)() | يزيل العلامة المائية. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage)(*Image*) | يضيف علامة مائية للصورة إلى المستند. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_1)(*Image, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | يضيف علامة مائية للصورة إلى المستند. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_2)(*Stream, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | يضيف علامة مائية للصورة إلى المستند. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_3)(*string, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | يضيف علامة مائية للصورة إلى المستند. |
| [SetText](../../aspose.words/watermark/settext/#settext)(*string*) | يضيف علامة مائية نصية إلى المستند. |
| [SetText](../../aspose.words/watermark/settext/#settext_1)(*string, [TextWatermarkOptions](../textwatermarkoptions/)*) | يضيف علامة مائية نصية إلى المستند. |

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
