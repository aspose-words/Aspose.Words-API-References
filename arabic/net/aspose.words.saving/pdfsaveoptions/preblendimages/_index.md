---
title: PdfSaveOptions.PreblendImages
linktitle: PreblendImages
articleTitle: PreblendImages
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PreblendImages في PdfSaveOptions. تحكم بسهولة في مزج الصور الشفافة لتحسين جودة المستند وجاذبيته البصرية.
type: docs
weight: 270
url: /ar/net/aspose.words.saving/pdfsaveoptions/preblendimages/
---
## PdfSaveOptions.PreblendImages property

يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم مزج الصور الشفافة مسبقًا مع لون الخلفية الأسود أم لا.

```csharp
public bool PreblendImages { get; set; }
```

## ملاحظات

قد يؤدي مزج الصور مسبقًا إلى تحسين المظهر المرئي لمستندات PDF في Adobe Reader وإزالة آثار التنعيم.

لعرض الصور الممزوجة مسبقًا بشكل صحيح، يجب أن يدعم تطبيق عارض PDF إدخال /Matte في قاموس الصور ذات القناع الناعم. كما أن المزج المسبق للصور قد يؤدي إلى تقليل أداء عرض PDF.

القيمة الافتراضية هي`خطأ شنيع`.

## أمثلة

يوضح كيفية دمج الصور مسبقًا مع الخلفيات الشفافة أثناء حفظ مستند بتنسيق PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Transparent background logo.png");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// اضبط خاصية "PreblendImages" على "true" لمزج الصور الشفافة مسبقًا
// مع خلفية، والتي قد تقلل من القطع الأثرية.
// اضبط خاصية "PreblendImages" على "false" لعرض الصور الشفافة بشكل طبيعي.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImages.pdf", options);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
