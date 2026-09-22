---
title: "تعداد Aspose::Words::Drawing::ShapeMarkupLanguage"
linktitle: "ShapeMarkupLanguage"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "تعداد Aspose::Words::Drawing::ShapeMarkupLanguage. يحدد لغة الترميز المستخدمة للشكل في C++."
type: docs
weight: 37000
url: /ar/cpp/aspose.words.drawing/shapemarkuplanguage/
---
## ShapeMarkupLanguage enum


يحدد لغة [Markup](../../aspose.words.markup/) المستخدمة للشكل.

```cpp
enum class ShapeMarkupLanguage : uint8_t
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Dml | 0 | يُستخدم [Drawing](../)[Markup](../../aspose.words.markup/) Language لتحديد الشكل. |
| Vml | 1 | لغة Vector [Markup](../../aspose.words.markup/) تُستخدم لتحديد الشكل. |


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

## انظر أيضًا

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
