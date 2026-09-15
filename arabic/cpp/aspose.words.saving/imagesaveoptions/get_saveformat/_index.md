---
title: "طريقة Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat"
linktitle: "get_SaveFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat. يحدد الصيغة التي سيتم حفظ صفحات المستند أو الأشكال المُصوَّرة فيها إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن تكون صيغ نقطية مثل Tiff، Png، Bmp، Jpeg أو صيغ متجهة مثل Emf، Eps، WebP، Svg في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words.saving/imagesaveoptions/get_saveformat/
---
## ImageSaveOptions::get_SaveFormat method


يحدد الصيغة التي سيتم حفظ صفحات المستند أو الأشكال المُصوَّرة فيها إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن تكون صيغ نقطية مثل [Tiff](../../../aspose.words/saveformat/)، [Png](../../../aspose.words/saveformat/)، [Bmp](../../../aspose.words/saveformat/)، [Jpeg](../../../aspose.words/saveformat/) أو صيغ متجهة مثل [Emf](../../../aspose.words/saveformat/), [Eps](../../../aspose.words/saveformat/), [WebP](../), [Svg](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat() override
```

## ملاحظات


عدد الخيارات الأخرى يعتمد على الصيغة المحددة.

كما يمكن حفظ إلى SVG إما عبر [ImageSaveOptions](../) أو عبر [SvgSaveOptions](../../svgsaveoptions/).

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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
