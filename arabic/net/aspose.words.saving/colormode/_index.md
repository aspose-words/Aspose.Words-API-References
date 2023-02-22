---
title: Enum ColorMode
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.ColorMode تعداد. يحدد كيفية عرض الألوان .
type: docs
weight: 4600
url: /ar/net/aspose.words.saving/colormode/
---
## ColorMode enumeration

يحدد كيفية عرض الألوان .

```csharp
public enum ColorMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Normal | `0` | التقديم بألوان غير معدلة. |
| Grayscale | `1` | عرض بألوان في مجموعة من الظلال الرمادية من الأبيض إلى الأسود. |

### أمثلة

يوضح كيفية تغيير لون الصورة باستخدام خاصية خيارات الحفظ.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
// اضبط خاصية "ColorMode" على "Grayscale" لعرض كل الصور من المستند بالأبيض والأسود.
// قد يكون حجم المستند الناتج أكبر مع هذا الإعداد.
// اضبط خاصية "ColorMode" على "عادي" لتقديم كل الصور بالألوان.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


