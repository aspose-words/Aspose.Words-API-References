---
title: FixedPageSaveOptions.ColorMode
second_title: Aspose.Words لمراجع .NET API
description: FixedPageSaveOptions ملكية. الحصول على أو تعيين قيمة تحدد كيفية عرض الألوان .
type: docs
weight: 10
url: /ar/net/aspose.words.saving/fixedpagesaveoptions/colormode/
---
## FixedPageSaveOptions.ColorMode property

الحصول على أو تعيين قيمة تحدد كيفية عرض الألوان .

```csharp
public ColorMode ColorMode { get; set; }
```

### ملاحظات

النظام الأساسيNormal .

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

* enum [ColorMode](../../colormode/)
* class [FixedPageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../fixedpagesaveoptions/)
* المجسم [Aspose.Words](../../../)


