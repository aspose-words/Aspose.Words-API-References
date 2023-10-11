---
title: MetafileRenderingOptions.UseGdiRasterOperationsEmulation
second_title: Aspose.Words لمراجع .NET API
description: MetafileRenderingOptions ملكية. الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم استخدام GDI لمحاكاة العمليات النقطية أم لا.
type: docs
weight: 80
url: /ar/net/aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/
---
## MetafileRenderingOptions.UseGdiRasterOperationsEmulation property

الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم استخدام GDI+ لمحاكاة العمليات النقطية أم لا.

```csharp
public bool UseGdiRasterOperationsEmulation { get; set; }
```

### ملاحظات

يمكن استخدام مكتبة Windows GDI+ لمحاكاة العمليات النقطية. وهو يوفر الدعم لجميع عمليات البيانات النقطية مقارنة بمحاكاة Aspose.Words الخاصة ولكن الأداء قد يكون أبطأ في بعض الحالات.

عندما يتم ضبط هذه القيمة على`حقيقي`، يستخدم Aspose.Words GDI+ لمحاكاة العمليات النقطية.

عندما يتم ضبط هذه القيمة على`خطأ شنيع`يستخدم Aspose.Words تطبيقه الخاص لمحاكاة العمليات النقطية.

يتم استخدام هذا الخيار فقط عندما يتم عرض ملف التعريف كرسومات متجهة.

القيمة الافتراضية هي`خطأ شنيع`.

### أمثلة

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

* class [MetafileRenderingOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../metafilerenderingoptions/)
* المجسم [Aspose.Words](../../../)


