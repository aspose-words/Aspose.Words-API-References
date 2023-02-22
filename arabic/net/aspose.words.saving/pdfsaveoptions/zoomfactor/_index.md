---
title: PdfSaveOptions.ZoomFactor
second_title: Aspose.Words لمراجع .NET API
description: PdfSaveOptions ملكية. الحصول على أو تعيين قيمة تحدد عامل التكبير / التصغير بالنسبة المئوية لمستند.
type: docs
weight: 300
url: /ar/net/aspose.words.saving/pdfsaveoptions/zoomfactor/
---
## PdfSaveOptions.ZoomFactor property

الحصول على أو تعيين قيمة تحدد عامل التكبير / التصغير (بالنسبة المئوية) لمستند.

```csharp
public int ZoomFactor { get; set; }
```

### ملاحظات

يتم استخدام هذه القيمة فقط إذا[`ZoomBehavior`](../zoombehavior/) تم تعيينه علىZoomFactor .

### أمثلة

يوضح كيفية تعيين التكبير الافتراضي الذي يطبقه القارئ عند فتح مستند PDF مقدم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
// قم بتعيين خاصية "ZoomBehavior" على "PdfZoomBehavior.ZoomFactor" للحصول على قارئ PDF
// قم بتطبيق عامل تكبير على أساس النسبة المئوية عندما نفتح المستند به.
// اضبط خاصية "ZoomFactor" على "25" لمنح عامل التكبير / التصغير قيمة 25٪.
PdfSaveOptions options = new PdfSaveOptions
{
    ZoomBehavior = PdfZoomBehavior.ZoomFactor,
    ZoomFactor = 25
};

// عندما نفتح هذا المستند باستخدام قارئ مثل Adobe Acrobat ، سنرى المستند بحجم 1/4 من حجمه الفعلي.
doc.Save(ArtifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../pdfsaveoptions/)
* المجسم [Aspose.Words](../../../)


