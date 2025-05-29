---
title: MetafileRenderingOptions.UseGdiRasterOperationsEmulation
linktitle: UseGdiRasterOperationsEmulation
articleTitle: UseGdiRasterOperationsEmulation
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية MetafileRenderingOptions UseGdiRasterOperationsEmulation لتحسين عمليات الراستر باستخدام GDI. حسّن الأداء والمرونة اليوم!
type: docs
weight: 80
url: /ar/net/aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/
---
## MetafileRenderingOptions.UseGdiRasterOperationsEmulation property

يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم استخدام GDI+ لمحاكاة عمليات الراستر أم لا.

```csharp
public bool UseGdiRasterOperationsEmulation { get; set; }
```

## ملاحظات

يمكن استخدام مكتبة Windows GDI+ لمحاكاة عمليات الراستر. تدعم المكتبة جميع عمليات الراستر مقارنةً بمحاكاة Aspose.Words، ولكن قد يكون الأداء أبطأ في بعض الحالات.

عندما يتم تعيين هذه القيمة على`حقيقي`يستخدم Aspose.Words GDI+ لمحاكاة عمليات الراستر.

عندما يتم تعيين هذه القيمة على`خطأ شنيع`يستخدم Aspose.Words تنفيذه الخاص لمحاكاة عمليات الراستر.

يتم استخدام هذا الخيار فقط عندما يتم عرض الملف التعريفي كرسومات متجهة.

القيمة الافتراضية هي`خطأ شنيع`.

## أمثلة

يوضح كيفية تعيين وضع العرض عند حفظ المستندات باستخدام صور Windows Metafile إلى تنسيقات صور أخرى.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Windows MetaFile.wmf");

// عندما نحفظ المستند كصورة، يمكننا تمرير كائن SaveOptions إلى
// تحديد كيفية معالجة عملية الحفظ لملفات Windows Metafiles في المستند.
// إذا قمنا بتعيين خاصية "RenderingMode" إلى "MetafileRenderingMode.Vector"،
// أو "MetafileRenderingMode.VectorWithFallback"، سنقوم بتقديم كافة الملفات التعريفية كرسومات متجهة.
// إذا قمنا بتعيين خاصية "RenderingMode" إلى "MetafileRenderingMode.Bitmap"، فسوف نقوم بعرض جميع الملفات التعريفية كخرائط بتات.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.MetafileRenderingOptions.RenderingMode = metafileRenderingMode;
// يستخدم Aspose.Words GDI+ لمحاكاة عمليات الراستر، عندما يتم تعيين القيمة على true.
options.MetafileRenderingOptions.UseGdiRasterOperationsEmulation = true;

doc.Save(ArtifactsDir + "ImageSaveOptions.WindowsMetaFile.png", options);
```

### أنظر أيضا

* class [MetafileRenderingOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
