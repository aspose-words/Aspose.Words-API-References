---
title: WatermarkLayout Enum
linktitle: WatermarkLayout
articleTitle: WatermarkLayout
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.WatermarkLayout لتحديد موضع العلامة المائية الأمثل. حسّن تصميم مستندك بتحكم دقيق في التخطيط وتخصيصه.
type: docs
weight: 7530
url: /ar/net/aspose.words/watermarklayout/
---
## WatermarkLayout enumeration

يحدد تخطيط العلامة المائية بالنسبة لمركز العلامة المائية.

```csharp
public enum WatermarkLayout
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Horizontal | `0` | تصميم علامة مائية أفقية. يتوافق مع 0 درجة دوران. |
| Diagonal | `315` | تصميم علامة مائية قطري. يتوافق مع دوران ٣١٥ درجة. |

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
