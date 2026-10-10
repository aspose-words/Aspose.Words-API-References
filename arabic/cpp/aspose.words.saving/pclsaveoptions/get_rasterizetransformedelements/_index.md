---
title: "طريقة Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements"
linktitle: "get_RasterizeTransformedElements"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements. يحصل أو يعيّن قيمة تحدد ما إذا كان يجب تحويل العناصر المعقدة إلى نقطية قبل الحفظ إلى مستند PCL. القيمة الافتراضية هي true في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.saving/pclsaveoptions/get_rasterizetransformedelements/
---
## PclSaveOptions::get_RasterizeTransformedElements method


يحصل أو يعيّن قيمة تحدد ما إذا كان يجب تحويل العناصر المعقدة إلى نقطية قبل حفظها في مستند PCL أم لا. القيمة الافتراضية هي **true**.

```cpp
bool Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements() const
```


## أمثلة



يظهر كيفية تحويل العناصر المعقدة إلى نقطية أثناء حفظ مستند إلى PCL.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Pcl);
saveOptions->set_RasterizeTransformedElements(true);

doc->Save(get_ArtifactsDir() + u"PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

## انظر أيضًا

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
