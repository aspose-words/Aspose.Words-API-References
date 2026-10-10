---
title: "Aspose::Words::Saving::ImageSaveOptions::get_ImageSize طريقة"
linktitle: "get_ImageSize"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_ImageSize طريقة. يحصل على أو يضبط حجم الصورة المولدة بالبكسل في C++."
type: docs
weight: 7500
url: /ar/cpp/aspose.words.saving/imagesaveoptions/get_imagesize/
---
## ImageSaveOptions::get_ImageSize method


يحصل أو يضبط حجم الصورة المُولَّدة بالبكسل.

```cpp
System::Drawing::Size Aspose::Words::Saving::ImageSaveOptions::get_ImageSize() const
```

## ملاحظات


هذه الخاصية لها تأثير فقط عند الحفظ إلى صيغ الصور النقطية.

القيمة الافتراضية هي (0 x 0)، مما يعني أن حجم الصورة المولدة سيُحسب وفقًا لحجم الصورة بالنقاط، والدقة المحددة، والقياس.

## أمثلة



يوضح كيفية تحويل كل صفحة من مستند إلى صورة TIFF منفصلة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// إنشاء كائن "ImageSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل الطريقة التي تقوم بها تلك الطريقة بتحويل المستند إلى صورة.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);

for (int32_t i = 0; i < doc->get_PageCount(); i++)
{
    // قم بتعيين الخاصية \"PageSet\" إلى رقم الصفحة الأولى من
    // التي يبدأ منها عرض المستند.
    options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(i));
    // تصدير الصفحة بدقة 2325x5325 بكسل و600 نقطة في البوصة.
    options->set_Resolution(600.0f);
    options->set_ImageSize(System::Drawing::Size(2325, 5325));

    doc->Save(get_ArtifactsDir() + System::String::Format(u"ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
}
```

## انظر أيضًا

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
