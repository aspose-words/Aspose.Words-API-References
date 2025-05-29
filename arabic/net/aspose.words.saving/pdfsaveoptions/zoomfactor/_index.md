---
title: PdfSaveOptions.ZoomFactor
linktitle: ZoomFactor
articleTitle: ZoomFactor
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ZoomFactor في PdfSaveOptions لضبط مستويات تكبير المستندات بسهولة بنسب مئوية، مما يعزز تجربة عرض ملفات PDF الخاصة بك.
type: docs
weight: 360
url: /ar/net/aspose.words.saving/pdfsaveoptions/zoomfactor/
---
## PdfSaveOptions.ZoomFactor property

يحصل على قيمة لتحديد عامل التكبير (بالنسب المئوية) لمستند أو يعينها.

```csharp
public int ZoomFactor { get; set; }
```

## ملاحظات

يتم استخدام هذه القيمة فقط إذا[`ZoomBehavior`](../zoombehavior/) تم ضبطه علىZoomFactor .

## أمثلة

يوضح كيفية تعيين التكبير الافتراضي الذي يطبقه القارئ عند فتح مستند PDF المقدم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
// اضبط خاصية "ZoomBehavior" على "PdfZoomBehavior.ZoomFactor" للحصول على قارئ PDF
// تطبيق عامل تكبير يعتمد على النسبة المئوية عند فتح المستند به.
// قم بضبط خاصية "ZoomFactor" على "25" لإعطاء عامل التكبير قيمة 25%.
PdfSaveOptions options = new PdfSaveOptions
{
    ZoomBehavior = PdfZoomBehavior.ZoomFactor,
    ZoomFactor = 25
};

// عندما نفتح هذا المستند باستخدام قارئ مثل Adobe Acrobat، سنرى المستند بحجم 1/4 من حجمه الفعلي.
doc.Save(ArtifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
