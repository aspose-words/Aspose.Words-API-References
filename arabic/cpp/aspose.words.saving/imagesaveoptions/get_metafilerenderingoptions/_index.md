---
title: "طريقة Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions"
linktitle: "get_MetafileRenderingOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions. يسمح بتحديد كيفية معالجة ملفات الميتافايل في المخرجات المُصوَّرة في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.saving/imagesaveoptions/get_metafilerenderingoptions/
---
## ImageSaveOptions::get_MetafileRenderingOptions method


يسمح بتحديد كيفية معالجة ملفات التعريف في الناتج المعروض.

```cpp
System::SharedPtr<Aspose::Words::Saving::MetafileRenderingOptions> Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions()
```

## ملاحظات


عند تحديد [Vector](../../metafilerenderingmode/)، يقوم Aspose.Words بتحويل ملف الميتافايل إلى رسومات متجهة باستخدام محرك التحويل الخاص به أولاً ثم يحول الرسومات المتجهة إلى الصورة.

عند تحديد [Bitmap](../../metafilerenderingmode/)، يقوم Aspose.Words بتحويل ملف الميتافايل مباشرة إلى الصورة باستخدام محرك التحويل GDI+ للميتافايل.

محرك التحويل GDI+ للميتافايل يعمل أسرع، يدعم تقريباً جميع ميزات الميتافايل ولكن عند الدقة المنخفضة قد ينتج نتيجة غير متسقة مقارنة ببقية الرسومات المتجهة (خاصةً للنص) على الصفحة. محرك التحويل الخاص بـ Aspose.Words للميتافايل سيُنتج نتيجة أكثر اتساقاً حتى في الدقة المنخفضة لكنه يعمل أبطأ وقد يُظهر ملفات ميتافايل معقدة بشكل غير دقيق.

القيمة الافتراضية لـ [MetafileRenderingMode](../../metafilerenderingmode/) هي [Bitmap](../../metafilerenderingmode/).

## أمثلة



يعرض كيفية ضبط وضعية العرض عند حفظ المستندات التي تحتوي على صور Windows Metafile إلى صيغ صور أخرى.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf");

// عند حفظ المستند كصورة، يمكننا تمرير كائن SaveOptions إلى
// تحديد كيفية معالجة عملية الحفظ لملفات Windows Metafile في المستند.
// إذا قمنا بتعيين خاصية "RenderingMode" إلى "MetafileRenderingMode.Vector",
// أو "MetafileRenderingMode.VectorWithFallback"، سنقوم بعرض جميع ملفات الميتا كرسومات متجهية.
// إذا قمنا بتعيين خاصية "RenderingMode" إلى "MetafileRenderingMode.Bitmap"، سنعرض جميع ملفات الميتا كصور نقطية.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
options->get_MetafileRenderingOptions()->set_RenderingMode(metafileRenderingMode);
// تستخدم Aspose.Words تقنية GDI+ لمحاكاة عمليات النقطية، عندما يتم تعيين القيمة إلى true.
options->get_MetafileRenderingOptions()->set_UseGdiRasterOperationsEmulation(true);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.WindowsMetaFile.png", options);
```

## انظر أيضًا

* Class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
