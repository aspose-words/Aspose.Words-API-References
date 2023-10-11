---
title: FixedPageSaveOptions.ColorMode
second_title: Aspose.Words لمراجع .NET API
description: FixedPageSaveOptions ملكية. الحصول على أو تعيين قيمة تحدد كيفية عرض الألوان.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/fixedpagesaveoptions/colormode/
---
## FixedPageSaveOptions.ColorMode property

الحصول على أو تعيين قيمة تحدد كيفية عرض الألوان.

```csharp
public ColorMode ColorMode { get; set; }
```

### ملاحظات

القيمة الافتراضية هيNormal .

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

* enum [ColorMode](../../colormode/)
* class [FixedPageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../fixedpagesaveoptions/)
* المجسم [Aspose.Words](../../../)


