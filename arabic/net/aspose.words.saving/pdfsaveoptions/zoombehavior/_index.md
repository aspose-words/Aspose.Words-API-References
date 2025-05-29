---
title: PdfSaveOptions.ZoomBehavior
linktitle: ZoomBehavior
articleTitle: ZoomBehavior
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ZoomBehavior في PdfSaveOptions، وتحكم في إعدادات التكبير/التصغير لعرض مثالي في عارضات PDF. حسّن تجربة المستخدم مع عرض مُخصص للمستندات!
type: docs
weight: 350
url: /ar/net/aspose.words.saving/pdfsaveoptions/zoombehavior/
---
## PdfSaveOptions.ZoomBehavior property

يحصل على قيمة أو يعينها لتحديد نوع التكبير الذي يجب تطبيقه عند فتح مستند باستخدام عارض PDF.

```csharp
public PdfZoomBehavior ZoomBehavior { get; set; }
```

## ملاحظات

القيمة الافتراضية هيNone ، أي أنه لا يتم تطبيق أي ملاءمة.

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

* enum [PdfZoomBehavior](../../pdfzoombehavior/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
