---
title: "طريقة Aspose::Words::Saving::ImageSaveOptions::set_Resolution"
linktitle: "set_Resolution"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::ImageSaveOptions::set_Resolution. يضبط كلًا من الدقة الأفقية والرأسية للصور المُنشأة، بوحدة النقاط في البوصة في C++."
type: docs
weight: 30000
url: /ar/cpp/aspose.words.saving/imagesaveoptions/set_resolution/
---
## ImageSaveOptions::set_Resolution method


يضبط كلًا من الدقة الأفقية والعمودية للصور المُولَّدة، بوحدة النقاط في البوصة.

```cpp
void Aspose::Words::Saving::ImageSaveOptions::set_Resolution(float value)
```

## ملاحظات


هذه الخاصية لها تأثير فقط عند الحفظ إلى صيغ الصور النقطية.

## أمثلة



يوضح كيفية تحديد الدقة أثناء تحويل المستند إلى PNG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// إنشاء كائن "ImageSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل الطريقة التي تقوم بها تلك الطريقة بتحويل المستند إلى صورة.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// اضبط الخاصية "Resolution" إلى "72" لتحويل المستند بدقة 72dpi.
options->set_Resolution(72.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.72dpi.png", options);

// اضبط الخاصية "Resolution" إلى "300" لتحويل المستند بدقة 300dpi.
options->set_Resolution(300.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.300dpi.png", options);
```

## انظر أيضًا

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
