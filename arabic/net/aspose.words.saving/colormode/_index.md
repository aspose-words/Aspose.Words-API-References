---
title: Enum ColorMode
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.ColorMode تعداد. يحدد كيفية عرض الألوان.
type: docs
weight: 4860
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
| Normal | `0` | العرض بألوان غير معدلة. |
| Grayscale | `1` | تقديم الألوان في مجموعة من الظلال الرمادية من الأبيض إلى الأسود. |

### أمثلة

يوضح كيفية تغيير لون الصورة مع خاصية خيارات الحفظ.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
// اضبط خاصية "ColorMode" على "تدرج الرمادي" لعرض جميع الصور من المستند باللونين الأبيض والأسود.
// قد يكون حجم مستند الإخراج أكبر مع هذا الإعداد.
// اضبط خاصية "ColorMode" على "عادي" لعرض جميع الصور بالألوان.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


