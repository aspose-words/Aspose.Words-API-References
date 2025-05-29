---
title: PdfSaveOptions.InterpolateImages
linktitle: InterpolateImages
articleTitle: InterpolateImages
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية InterpolateImages في PdfSaveOptions، وهي ميزة أساسية تُحسّن جودة الصور في مستنداتك. حسّن ملفات PDF الخاصة بك بسهولة!
type: docs
weight: 210
url: /ar/net/aspose.words.saving/pdfsaveoptions/interpolateimages/
---
## PdfSaveOptions.InterpolateImages property

علم يشير إلى ما إذا كان سيتم تنفيذ استيفاء الصورة بواسطة قارئ متوافق. عندما`خطأ شنيع` إذا تم تحديد ذلك، فلن تتم كتابة العلم في مستند الإخراج وسيتم استخدام السلوك الافتراضي للقارئ بدلاً من ذلك.

```csharp
public bool InterpolateImages { get; set; }
```

## ملاحظات

عندما تكون دقة صورة المصدر أقل بكثير من دقة جهاز الإخراج، تغطي كل عينة مصدر العديد من وحدات بكسل الجهاز. ونتيجة لذلك، قد تظهر الصور متقطعة أو متكتلة. يمكن تقليل هذه العيوب البصرية بتطبيق خوارزمية استيفاء الصور أثناء العرض. بدلاً من طلاء جميع وحدات البكسل التي تغطيها عينة المصدر بنفس اللون، تحاول عملية استيفاء الصور إنشاء انتقال سلس بين قيم العينات المتجاورة.

يمكن للقارئ المطابق اختيار عدم تنفيذ هذه الميزة في PDF، أو استخدام أي تنفيذ محدد للتدخل يرغب فيه.

القيمة الافتراضية هي`خطأ شنيع`.

يُحظر استخدام علم الاستيفاء بموجب التوافق مع PDF/A.`خطأ شنيع` سيتم استخدام القيمة تلقائيًا عند الحفظ في PDF/A.

## أمثلة

يوضح كيفية إجراء الاستيفاء على الصور أثناء حفظ مستند بتنسيق PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Transparent background logo.png");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// قم بضبط خاصية "InterpolateImages" على "true" لجعل القارئ الذي يفتح هذا المستند يقوم باستيفاء الصور.
//يجب أن تكون دقتها أقل من دقة الجهاز الذي يعرض المستند.
// قم بضبط خاصية "InterpolateImages" على "false" لجعل القارئ لا يطبق أي استيفاء.
saveOptions.InterpolateImages = interpolateImages;

// عندما نفتح هذا المستند باستخدام قارئ مثل Adobe Acrobat، سنحتاج إلى تكبير الصورة
// لرؤية تأثير الاستيفاء إذا قمنا بحفظ المستند مع تمكينه.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImages.pdf", saveOptions);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
