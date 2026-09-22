---
title: "طريقة Aspose::Words::Saving::ImageSaveOptions::get_Scale"
linktitle: "get_Scale"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::ImageSaveOptions::get_Scale. يحصل على أو يضبط عامل التكبير للصور المولدة في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words.saving/imagesaveoptions/get_scale/
---
## ImageSaveOptions::get_Scale method


يحصل أو يضبط عامل التكبير للصور المُولَّدة.

```cpp
float Aspose::Words::Saving::ImageSaveOptions::get_Scale() const
```


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


يوضح كيفية تحويل كائن Office [Math](../../../aspose.words.math/) إلى ملف صورة في نظام الملفات المحلي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// أنشئ كائن "ImageSaveOptions" لتمريره إلى طريقة "Save" الخاصة بالمُعالج العقدة لتعديل
// كيفية تصييره لعقدة OfficeMath إلى صورة.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// اضبط خاصية "Scale" إلى 5 لتصوير الكائن بمقاس يساوي خمسة أضعاف حجمه الأصلي.
saveOptions->set_Scale(5.0f);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"Shape.RenderOfficeMath.png", saveOptions);
```

## انظر أيضًا

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
