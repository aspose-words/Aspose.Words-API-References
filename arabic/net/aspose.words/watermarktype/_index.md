---
title: Enum WatermarkType
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.WatermarkType تعداد. يحدد نوع العلامة المائية.
type: docs
weight: 6690
url: /ar/net/aspose.words/watermarktype/
---
## WatermarkType enumeration

يحدد نوع العلامة المائية.

```csharp
public enum WatermarkType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Text | `0` | يشير إلى أنه سيتم استخدام النص كعلامة مائية. |
| Image | `1` | يشير إلى أنه سيتم استخدام الصورة كعلامة مائية. |
| None | `2` | يشير إلى عدم تعيين العلامة المائية. |

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


