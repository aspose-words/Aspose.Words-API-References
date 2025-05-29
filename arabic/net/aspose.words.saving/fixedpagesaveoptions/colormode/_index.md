---
title: FixedPageSaveOptions.ColorMode
linktitle: ColorMode
articleTitle: ColorMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ColorMode في FixedPageSaveOptions لتخصيص عرض الألوان لتحسين جودة المستند وجاذبيته البصرية. حسّن إنتاجيتك اليوم!
type: docs
weight: 10
url: /ar/net/aspose.words.saving/fixedpagesaveoptions/colormode/
---
## FixedPageSaveOptions.ColorMode property

يحصل على قيمة تحدد كيفية عرض الألوان أو يعينها.

```csharp
public ColorMode ColorMode { get; set; }
```

## ملاحظات

القيمة الافتراضية هيNormal .

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

* enum [ColorMode](../../colormode/)
* class [FixedPageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
