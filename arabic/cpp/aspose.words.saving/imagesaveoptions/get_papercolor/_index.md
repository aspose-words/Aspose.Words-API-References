---
title: "Aspose::Words::Saving::ImageSaveOptions::get_PaperColor طريقة"
linktitle: "get_PaperColor"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_PaperColor طريقة. يحصل أو يضبط لون الخلفية (الورق) للصور المُنشأة. القيمة الافتراضية هي White في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words.saving/imagesaveoptions/get_papercolor/
---
## ImageSaveOptions::get_PaperColor method


يحصل أو يضبط لون الخلفية (الورق) للصور المُولَّدة. القيمة الافتراضية هي **White**.

```cpp
System::Drawing::Color Aspose::Words::Saving::ImageSaveOptions::get_PaperColor()
```

## ملاحظات


عند عرض صفحات مستند يحدد لون خلفيته الخاص، سيتجاوز لون خلفية المستند اللون المحدد بهذه الخاصية.

## أمثلة



يُصوّر صفحة من مستند Word إلى صورة بخلفية شفافة أو ملونة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// إنشاء كائن "ImageSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل الطريقة التي تقوم بها تلك الطريقة بتحويل المستند إلى صورة.
auto imgOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// اضبط الخاصية "PaperColor" إلى لون شفاف لتطبيق شفاف
// خلفية للمستند أثناء تحويله إلى صورة.
imgOptions->set_PaperColor(System::Drawing::Color::get_Transparent());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// اضبط الخاصية "PaperColor" إلى لون غير شفاف لتطبيق ذلك اللون
// كخلفية للمستند أثناء تحويله إلى صورة.
imgOptions->set_PaperColor(System::Drawing::Color::get_LightCoral());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

## انظر أيضًا

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
