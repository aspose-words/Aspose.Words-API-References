---
title: Enum PdfZoomBehavior
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.PdfZoomBehavior تعداد. يحدد نوع التكبير/التصغير المطبق على مستند PDF عند فتحه في عارض PDF.
type: docs
weight: 5540
url: /ar/net/aspose.words.saving/pdfzoombehavior/
---
## PdfZoomBehavior enumeration

يحدد نوع التكبير/التصغير المطبق على مستند PDF عند فتحه في عارض PDF.

```csharp
public enum PdfZoomBehavior
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | كيفية عرض الوثيقة متروكة لعارض PDF. عادةً ما يقوم العارض بعرض المستند ليناسب عرض الصفحة. |
| ZoomFactor | `1` | يعرض الصفحة باستخدام عامل التكبير/التصغير المحدد. |
| FitPage | `2` | عرض الصفحة بحيث تكون مرئية بالكامل. |
| FitWidth | `3` | يناسب عرض الصفحة. |
| FitHeight | `4` | يناسب ارتفاع الصفحة. |
| FitBox | `5` | يناسب المربع المحيط (المستطيل الذي يحتوي على كافة العناصر المرئية في الصفحة). |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


