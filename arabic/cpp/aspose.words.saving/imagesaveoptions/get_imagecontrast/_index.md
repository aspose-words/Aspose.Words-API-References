---
title: "طريقة Aspose::Words::Saving::ImageSaveOptions::get_ImageContrast"
linktitle: "get_ImageContrast"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::ImageSaveOptions::get_ImageContrast. يحصل أو يضبط التباين للصور المُنشأة في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.saving/imagesaveoptions/get_imagecontrast/
---
## ImageSaveOptions::get_ImageContrast method


يحصل أو يضبط التباين للصور المُولَّدة.

```cpp
float Aspose::Words::Saving::ImageSaveOptions::get_ImageContrast() const
```

## ملاحظات


هذه الخاصية لها تأثير فقط عند الحفظ إلى صيغ الصور النقطية.

القيمة الافتراضية هي 0.5. يجب أن تكون القيمة في النطاق بين 0 و 1.

## أمثلة



يظهر كيفية تعديل الصورة بينما يقوم Aspose.Words بتحويل المستند إلى صورة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// عند حفظ المستند كصورة، يمكننا تمرير كائن SaveOptions إلى
// تحرير الصورة بينما عملية الحفظ تعرضها.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// يمكننا تعديل هذه الخصائص لتغيير سطوع الصورة وتباينها.
// كلاهما على مقياس من 0 إلى 1 ويكونان عند 0.5 افتراضيًا.
options->set_ImageBrightness(0.3f);
options->set_ImageContrast(0.7f);
// يمكننا تعديل الدقة الأفقية والعمودية باستخدام هذه الخصائص.
// سيؤثر هذا على أبعاد الصورة.
// القيمة الافتراضية لهذه الخصائص هي 96.0، لدقة 96dpi.
options->set_HorizontalResolution(72.f);
options->set_VerticalResolution(72.f);
// يمكننا تحجيم الصورة باستخدام هذه الخاصية. القيمة الافتراضية هي 1.0، لتحجيم بنسبة 100%.
// يمكننا استخدام هذه الخاصية لإلغاء أي تغييرات في أبعاد الصورة قد يسببها تغيير الدقة.
options->set_Scale(96.f / 72.f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.EditImage.png", options);
```

## انظر أيضًا

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
