---
title: WatermarkLayout Enum
linktitle: WatermarkLayout
articleTitle: WatermarkLayout
second_title: Aspose.Words لـ .NET
description: Aspose.Words.WatermarkLayout تعداد. يحدد تخطيط العلامة المائية بالنسبة لمركز العلامة المائية في C#.
type: docs
weight: 6680
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
| Horizontal | `0` | تخطيط العلامة المائية الأفقية. يتوافق مع 0 درجة من الدوران. |
| Diagonal | `315` | تخطيط العلامة المائية القطرية. يتوافق مع 315 درجة دوران. |

## أمثلة

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
