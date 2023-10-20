---
title: ImageSaveOptions.MetafileRenderingOptions
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words لـ .NET
description: ImageSaveOptions MetafileRenderingOptions ملكية. يسمح بتحديد كيفية التعامل مع ملفات التعريف في المخرجات المقدمة في C#.
type: docs
weight: 90
url: /ar/net/aspose.words.saving/imagesaveoptions/metafilerenderingoptions/
---
## ImageSaveOptions.MetafileRenderingOptions property

يسمح بتحديد كيفية التعامل مع ملفات التعريف في المخرجات المقدمة.

```csharp
public MetafileRenderingOptions MetafileRenderingOptions { get; }
```

## ملاحظات

متىVector تم تحديد Aspose.Words الذي يعرض ملف التعريف إلى رسومات متجهة باستخدام محرك عرض ملف التعريف الخاص به أولاً ثم يعرض رسومات Vector إلى الصورة.

متىBitmap تم تحديد Aspose.Words يعرض ملف التعريف مباشرة إلى الصورة باستخدام محرك عرض ملف التعريف GDI+.

يعمل محرك عرض ملف التعريف GDI+ بشكل أسرع، ويدعم جميع ميزات ملف التعريف تقريبًا، ولكن عند الدقة المنخفضة قد ينتج نتائج غير متناسقة عند مقارنتها ببقية الرسومات المتجهة (خاصة للنص) على الصفحة. سينتج محرك عرض ملف تعريف Aspose.Words نتيجة أكثر اتساقًا حتى على دقة منخفضة ولكنه يعمل بشكل أبطأ وقد يعرض ملفات تعريف معقدة بشكل غير دقيق.

القيمة الافتراضية ل[`MetafileRenderingMode`](../../metafilerenderingmode/) يكونBitmap.

## أمثلة

يوضح كيفية ضبط وضع العرض عند حفظ المستندات التي تحتوي على صور Windows Metafile إلى تنسيقات صور أخرى.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(Image.FromFile(ImageDir + "Windows MetaFile.wmf"));

// عندما نحفظ المستند كصورة، يمكننا تمرير كائن SaveOptions إليه
// تحديد كيفية معالجة عملية الحفظ لملفات تعريف Windows في المستند.
// إذا قمنا بتعيين خاصية "RenderingMode" على "MetafileRenderingMode.Vector"،
// أو "MetafileRenderingMode.VectorWithFallback"، سنعرض جميع ملفات التعريف كرسومات متجهة.
// إذا قمنا بتعيين خاصية "RenderingMode" على "MetafileRenderingMode.Bitmap"، فسنعرض كافة ملفات التعريف كصور نقطية.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.MetafileRenderingOptions.RenderingMode = metafileRenderingMode;
// Aspose.Words يستخدم GDI+ لمحاكاة العمليات النقطية، عندما يتم تعيين القيمة على true.
options.MetafileRenderingOptions.UseGdiRasterOperationsEmulation = true;

doc.Save(ArtifactsDir + "ImageSaveOptions.WindowsMetaFile.png", options);
```

### أنظر أيضا

* class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
