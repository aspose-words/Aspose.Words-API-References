---
title: ImageSaveOptions.MetafileRenderingOptions
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ImageSaveOptions MetafileRenderingOptions للتحكم في التعامل مع الملف التعريفي في المخرجات المقدمة لتحسين جودة الصورة.
type: docs
weight: 90
url: /ar/net/aspose.words.saving/imagesaveoptions/metafilerenderingoptions/
---
## ImageSaveOptions.MetafileRenderingOptions property

يسمح بتحديد كيفية التعامل مع الملفات التعريفية في المخرجات المقدمة.

```csharp
public MetafileRenderingOptions MetafileRenderingOptions { get; }
```

## ملاحظات

متىVector يتم تحديد ذلك، حيث يقوم Aspose.Words بعرض ملف التعريف x000d_ إلى رسومات متجهية باستخدام محرك عرض ملف التعريف الخاص به أولاً ثم يعرض رسومات vector إلى الصورة.

متىBitmap إذا تم تحديد ذلك، يقوم Aspose.Words بعرض ملف التعريف x000d_ مباشرةً على الصورة باستخدام محرك عرض ملف التعريف GDI+.

يعمل محرك عرض ملفات التعريف GDI+ بشكل أسرع، ويدعم جميع ميزات ملفات التعريف تقريبًا، ولكن عند استخدام دقة منخفضة x000d_ قد يُنتج نتائج غير متسقة مقارنةً ببقية الرسومات المتجهة (خاصةً للنصوص) x000d_ على الصفحة. يُنتج محرك عرض ملفات التعريف Aspose.Words نتائج أكثر اتساقًا حتى عند استخدام دقة منخفضة x000d_، ولكنه يعمل بشكل أبطأ وقد يُنتج ملفات تعريف معقدة بشكل غير دقيق.

القيمة الافتراضية لـ[`MetafileRenderingMode`](../../metafilerenderingmode/) يكونBitmap.

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

* class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
