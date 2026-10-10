---
title: "طريقة Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName"
linktitle: "get_FallbackFontName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName. اسم الخط الذي سيُستخدم إذا لم يُعثر على الخط المتوقع في طابعة ومجموعات الخطوط المدمجة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.saving/pclsaveoptions/get_fallbackfontname/
---
## PclSaveOptions::get_FallbackFontName method


اسم الخط الذي سيُستخدم إذا لم يتم العثور على الخط المتوقع في الطابعة ومجموعات الخطوط المدمجة.

```cpp
System::String Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName() const
```


## أمثلة



يظهر كيفية إعلان خط سيطبقه الطابعة على النص المطبوع كبديل إذا كان الخط الأصلي غير متوفر.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Non-existent font");
builder->Write(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->set_FallbackFontName(u"Times New Roman");

// سوف يوجه هذا المستند الطابعة لتطبيق "Times New Roman" على النص الذي يفتقد الخط.
// إذا كان "Times New Roman" غير متوفر أيضًا، ستعود الطابعة إلى الخط "Arial" افتراضيًا.
doc->Save(get_ArtifactsDir() + u"PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

## انظر أيضًا

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
