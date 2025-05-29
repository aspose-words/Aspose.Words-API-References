---
title: PdfZoomBehavior Enum
linktitle: PdfZoomBehavior
articleTitle: PdfZoomBehavior
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words.PdfZoomBehavior لإعدادات تكبير/تصغير قابلة للتخصيص في ملفات PDF. حسّن تجربة المستخدم مع خيارات عرض مُخصصة في مستندات PDF.
type: docs
weight: 6340
url: /ar/net/aspose.words.saving/pdfzoombehavior/
---
## PdfZoomBehavior enumeration

يحدد نوع التكبير المطبق على مستند PDF عند فتحه في عارض PDF.

```csharp
public enum PdfZoomBehavior
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | يُترك لعارض PDF تحديد كيفية عرض المستند. عادةً ما يعرض العارض المستند بما يتناسب مع عرض الصفحة. |
| ZoomFactor | `1` | يعرض الصفحة باستخدام عامل التكبير المحدد. |
| FitPage | `2` | يعرض الصفحة بحيث تكون مرئية بالكامل. |
| FitWidth | `3` | يتناسب مع عرض الصفحة. |
| FitHeight | `4` | يتناسب مع ارتفاع الصفحة. |
| FitBox | `5` | يتناسب مع المربع المحدد (المستطيل الذي يحتوي على جميع العناصر المرئية في الصفحة). |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
