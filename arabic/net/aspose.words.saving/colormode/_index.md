---
title: ColorMode Enum
linktitle: ColorMode
articleTitle: ColorMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words.Saving.ColorMode لتحسين عرض الألوان. حسّن مظهر مستندك بإعدادات ألوان دقيقة.
type: docs
weight: 5600
url: /ar/net/aspose.words.saving/colormode/
---
## ColorMode enumeration

يحدد كيفية عرض الألوان.

```csharp
public enum ColorMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Normal | `0` | العرض باستخدام الألوان غير المعدلة. |
| Grayscale | `1` | عرض الألوان في مجموعة من درجات اللون الرمادي من الأبيض إلى الأسود. |

## أمثلة

يوضح كيفية تغيير لون الصورة باستخدام خاصية خيارات الحفظ.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
// قم بضبط خاصية "ColorMode" على "Grayscale" لعرض كافة الصور من المستند باللونين الأبيض والأسود.
//قد يكون حجم المستند الناتج أكبر مع هذا الإعداد.
// اضبط خاصية "ColorMode" على "Normal" لعرض كافة الصور بالألوان.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
