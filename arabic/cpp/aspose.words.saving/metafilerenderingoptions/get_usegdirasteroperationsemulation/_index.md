---
title: "طريقة Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation"
linktitle: "get_UseGdiRasterOperationsEmulation"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation. يحصل أو يضبط قيمة تحدد ما إذا كان سيتم استخدام GDI+ لمحاكاة عمليات الرستر في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.saving/metafilerenderingoptions/get_usegdirasteroperationsemulation/
---
## MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation method


يحصل أو يعيّن قيمة تحدد ما إذا كان يجب استخدام GDI+ لمحاكاة عمليات الرستر أم لا.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation() const
```

## ملاحظات


يمكن استخدام مكتبة Windows GDI+ لمحاكاة عمليات الرستر. إنها توفر دعمًا لجميع عمليات الرستر مقارنةً بمحاكاة Aspose.Words الخاصة ولكن قد يكون الأداء أبطأ في بعض الحالات.

عند ضبط هذه القيمة إلى **true**، يستخدم Aspose.Words GDI+ لمحاكاة عمليات الرستر.

عند ضبط هذه القيمة إلى **false**، يستخدم Aspose.Words تنفيذه الخاص لمحاكاة عمليات الرستر.

يُستخدم هذا الخيار فقط عندما يتم تصيير ملف الميتا كرسومات متجهة.

القيمة الافتراضية هي **false**.

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

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
