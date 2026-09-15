---
title: "طريقة Aspose::Words::Saving::PclSaveOptions::get_SaveFormat"
linktitle: "get_SaveFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::PclSaveOptions::get_SaveFormat. تحدد الصيغة التي سيُحفظ بها المستند إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن تكون فقط Pcl في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.saving/pclsaveoptions/get_saveformat/
---
## PclSaveOptions::get_SaveFormat method


تحدد الصيغة التي سيُحفظ بها المستند إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن تكون فقط [Pcl](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::PclSaveOptions::get_SaveFormat() override
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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
