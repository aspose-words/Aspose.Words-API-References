---
title: PdfSaveOptions.ZoomBehavior
second_title: Aspose.Words لمراجع .NET API
description: PdfSaveOptions ملكية. الحصول على قيمة أو تعيينها لتحديد نوع التكبير/التصغير الذي يجب تطبيقه عند فتح مستند باستخدام عارض PDF.
type: docs
weight: 320
url: /ar/net/aspose.words.saving/pdfsaveoptions/zoombehavior/
---
## PdfSaveOptions.ZoomBehavior property

الحصول على قيمة أو تعيينها لتحديد نوع التكبير/التصغير الذي يجب تطبيقه عند فتح مستند باستخدام عارض PDF.

```csharp
public PdfZoomBehavior ZoomBehavior { get; set; }
```

### ملاحظات

القيمة الافتراضية هيNone ، أي لم يتم تطبيق أي ملاءمة.

### أمثلة

يوضح كيفية ضبط التكبير/التصغير الافتراضي الذي يطبقه القارئ عند فتح مستند PDF معروض.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
// اضبط خاصية "ZoomBehavior" على "PdfZoomBehavior.ZoomFactor" للحصول على قارئ PDF
// قم بتطبيق عامل التكبير على أساس النسبة المئوية عندما نفتح المستند به.
// اضبط خاصية "ZoomFactor" على "25" لإعطاء عامل التكبير قيمة 25%.
PdfSaveOptions options = new PdfSaveOptions
{
    ZoomBehavior = PdfZoomBehavior.ZoomFactor,
    ZoomFactor = 25
};

// عندما نفتح هذا المستند باستخدام قارئ مثل Adobe Acrobat، سنرى المستند بحجم 1/4 من حجمه الفعلي.
doc.Save(ArtifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### أنظر أيضا

* enum [PdfZoomBehavior](../../pdfzoombehavior/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../pdfsaveoptions/)
* المجسم [Aspose.Words](../../../)


