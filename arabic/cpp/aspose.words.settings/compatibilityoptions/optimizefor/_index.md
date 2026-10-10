---
title: "Aspose::Words::Settings::CompatibilityOptions::OptimizeFor طريقة"
linktitle: "OptimizeFor"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Settings::CompatibilityOptions::OptimizeFor طريقة. تسمح بتحسين محتويات المستند وكذلك سلوك Aspose.Words الافتراضي لإصدارات معينة من MS Word. استخدم هذه الطريقة لمنع MS Word من عرض شريط \"Compatibility mode\" عند تحميل المستند. (لاحظ أنك قد تحتاج أيضًا إلى تعيين خاصية Compliance إلى Iso29500_2008_Transitional أو أعلى.) في C++."
type: docs
weight: 75000
url: /ar/cpp/aspose.words.settings/compatibilityoptions/optimizefor/
---
## CompatibilityOptions::OptimizeFor method


يسمح بتحسين محتويات المستند وكذلك سلوك Aspose.Words الافتراضي لإصدارات معينة من MS Word. استخدم هذه الطريقة لمنع MS Word من عرض شريط "Compatibility mode" عند تحميل المستند. (لاحظ أنك قد تحتاج أيضًا إلى تعيين خاصية [Compliance](../../../aspose.words.saving/ooxmlsaveoptions/get_compliance/) إلى [Iso29500_2008_Transitional](../../../aspose.words.saving/ooxmlcompliance/) أو أعلى.)

```cpp
void Aspose::Words::Settings::CompatibilityOptions::OptimizeFor(Aspose::Words::Settings::MsWordVersion version)
```


## أمثلة



يوضح كيفية تعيين مواصفة امتثال OOXML لمستند محفوظ للالتزام بها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إذا قمنا بتكوين خيارات التوافق للامتثال مع Microsoft Word 2003،
// إدراج صورة سيحدد شكلها باستخدام VML.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Vml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());

// معيار OOXML "ISO/IEC 29500:2008" لا يدعم أشكال VML.
// إذا قمنا بتعيين خاصية "Compliance" لكائن SaveOptions إلى "OoxmlCompliance.Iso29500_2008_Strict",
// أي مستند نقوم بحفظه مع تمرير هذا الكائن سيتعين عليه اتباع ذلك المعيار.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docx);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// المستند المحفوظ لدينا يحدد الشكل باستخدام DML للالتزام بمعيار OOXML "ISO/IEC 29500:2008".
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());
```


يوضح كيفية محاذاة محتوى النص داخل صندوق النص عموديًا.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 200, 200);

// قم بتعيين الخاصية "VerticalAnchor" إلى "TextBoxAnchor.Top" لـ
// محاذاة النص في هذا الصندوق النصي مع الجانب العلوي للشكل.
// قم بتعيين الخاصية "VerticalAnchor" إلى "TextBoxAnchor.Middle" لـ
// محاذاة النص في هذا الصندوق النصي إلى مركز الشكل.
// قم بتعيين الخاصية "VerticalAnchor" إلى "TextBoxAnchor.Bottom" لـ
// محاذاة النص في هذا الصندوق النصي إلى أسفل الشكل.
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// تتوفر محاذاة النص عموديًا داخل صناديق النص منذ Microsoft Word 2007 وما بعده.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```

## انظر أيضًا

* Enum [MsWordVersion](../../mswordversion/)
* Class [CompatibilityOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
