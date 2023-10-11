---
title: PdfSaveOptions.PreblendImages
second_title: Aspose.Words لمراجع .NET API
description: PdfSaveOptions ملكية. الحصول على أو تعيين قيمة لتحديد ما إذا كان سيتم مزج الصور الشفافة مسبقًا مع لون الخلفية السوداء أم لا.
type: docs
weight: 260
url: /ar/net/aspose.words.saving/pdfsaveoptions/preblendimages/
---
## PdfSaveOptions.PreblendImages property

الحصول على أو تعيين قيمة لتحديد ما إذا كان سيتم مزج الصور الشفافة مسبقًا مع لون الخلفية السوداء أم لا.

```csharp
public bool PreblendImages { get; set; }
```

### ملاحظات

قد يؤدي المزج المسبق للصور إلى تحسين المظهر المرئي لمستندات PDF في Adobe Reader وإزالة العناصر المضادة للتعرجات.

من أجل عرض الصور الممزوجة مسبقًا بشكل صحيح، يجب أن يدعم تطبيق عارض PDF الإدخال /Matte في قاموس صور القناع الناعم. كما أن الصور الممزوجة مسبقًا قد تقلل من أداء عرض PDF.

القيمة الافتراضية هي`خطأ شنيع`.

### أمثلة

يوضح كيفية مزج الصور مسبقًا بخلفيات شفافة أثناء حفظ المستند في ملف PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image img = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.InsertImage(img);

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "PreblendImages" على "true" لمزج الصور الشفافة مسبقًا
// بخلفية قد تقلل من التحف.
// اضبط خاصية "PreblendImages" على "خطأ" لعرض الصور الشفافة بشكل طبيعي.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImages.pdf", options);
```

يوضح كيفية مزج الصور مسبقًا بخلفيات شفافة (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Image image = Image.Decode(ImageDir + "Transparent background logo.png"))
    builder.InsertImage(image);

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "PreblendImages" على "true" لمزج الصور الشفافة مسبقًا
// بخلفية قد تقلل من التحف.
// اضبط خاصية "PreblendImages" على "خطأ" لعرض الصور الشفافة بشكل طبيعي.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImagesNetStandard2.pdf", options);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../pdfsaveoptions/)
* المجسم [Aspose.Words](../../../)


