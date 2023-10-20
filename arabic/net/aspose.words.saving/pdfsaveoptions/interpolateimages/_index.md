---
title: PdfSaveOptions.InterpolateImages
linktitle: InterpolateImages
articleTitle: InterpolateImages
second_title: Aspose.Words لـ .NET
description: PdfSaveOptions InterpolateImages ملكية. علامة تشير إلى ما إذا كان سيتم تنفيذ استكمال الصورة بواسطة قارئ مطابق. متىخطأ شنيع تم تحديده ولم تتم كتابة العلامة في مستند الإخراج و يتم استخدام السلوك الافتراضي للقارئ بدلاً من ذلك في C#.
type: docs
weight: 210
url: /ar/net/aspose.words.saving/pdfsaveoptions/interpolateimages/
---
## PdfSaveOptions.InterpolateImages property

علامة تشير إلى ما إذا كان سيتم تنفيذ استكمال الصورة بواسطة قارئ مطابق. متى`خطأ شنيع` تم تحديده، ولم تتم كتابة العلامة في مستند الإخراج و يتم استخدام السلوك الافتراضي للقارئ بدلاً من ذلك.

```csharp
public bool InterpolateImages { get; set; }
```

## ملاحظات

عندما تكون دقة الصورة المصدر أقل بكثير من دقة جهاز الإخراج، تغطي كل عينة مصدر العديد من وحدات بكسل الجهاز. ونتيجة لذلك، يمكن أن تظهر الصور غير واضحة أو ممتلئة. يمكن تقليل هذه التأثيرات المرئية عن طريق تطبيق خوارزمية استيفاء الصورة أثناء العرض. بدلاً من طلاء جميع وحدات البكسل المغطاة بعينة مصدر بنفس اللون، يحاول استيفاء الصورة إنتاج صورة سلسة الانتقال بين قيم العينة المتجاورة.

قد يختار القارئ المطابق عدم تنفيذ هذه الميزة لملف PDF، أو يجوز له استخدام أي تطبيق محدد للاستيفاء الذي يرغب فيه.

القيمة الافتراضية هي`خطأ شنيع`.

علامة الاستيفاء محظورة بموجب الامتثال لـ PDF/A.`خطأ شنيع` سيتم استخدام القيمة تلقائيًا عند الحفظ في PDF/A.

## أمثلة

يوضح كيفية إجراء الاستيفاء على الصور أثناء حفظ مستند إلى PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image img = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.InsertImage(img);

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// اضبط خاصية "InterpolateImages" على "true" ليتمكن القارئ الذي يفتح هذا المستند من استيفاء الصور.
// يجب أن تكون دقتها أقل من دقة الجهاز الذي يعرض المستند.
// اضبط خاصية "InterpolateImages" على "خطأ" حتى لا يطبق القارئ أي استيفاء.
saveOptions.InterpolateImages = interpolateImages;

// عندما نفتح هذا المستند باستخدام قارئ مثل Adobe Acrobat، سنحتاج إلى تكبير الصورة
// لرؤية تأثير الاستيفاء إذا قمنا بحفظ المستند مع تمكينه.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImages.pdf", saveOptions);
```

يوضح كيفية تحسين جودة الصورة في المستندات المقدمة (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Image image = Image.Decode(ImageDir + "Transparent background logo.png"))
    builder.InsertImage(image);

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// اضبط خاصية "InterpolateImages" على "true" ليتمكن القارئ الذي يفتح هذا المستند من استيفاء الصور.
// يجب أن تكون دقتها أقل من دقة الجهاز الذي يعرض المستند.
// اضبط خاصية "InterpolateImages" على "خطأ" حتى لا يطبق القارئ أي استيفاء.
saveOptions.InterpolateImages = interpolateImages;

// عندما نفتح هذا المستند باستخدام قارئ مثل Adobe Acrobat، سنحتاج إلى تكبير الصورة
// لرؤية تأثير الاستيفاء إذا قمنا بحفظ المستند مع تمكينه.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImagesNetStandard2.pdf", saveOptions);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
