---
title: "Aspose::Words::Settings::ViewOptions::get_FormsDesign طريقة"
linktitle: "get_FormsDesign"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Settings::ViewOptions::get_FormsDesign طريقة. يحدد ما إذا كان المستند في وضع تصميم النماذج في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.settings/viewoptions/get_formsdesign/
---
## ViewOptions::get_FormsDesign method


يحدد ما إذا كان المستند في وضع تصميم النماذج.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_FormsDesign() const
```

## ملاحظات


يعمل حاليًا فقط مع المستندات بتنسيق WordML.

## أمثلة



يظهر كيفية تمكين/تعطيل وضع تصميم النماذج.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// عيّن الخاصية "FormsDesign" إلى "false" لإبقاء وضع تصميم النماذج معطلاً.
// عيّن الخاصية "FormsDesign" إلى "true" لتمكين وضع تصميم النماذج.
doc->get_ViewOptions()->set_FormsDesign(useFormsDesign);

doc->Save(get_ArtifactsDir() + u"ViewOptions.FormsDesign.xml");

ASPOSE_ASSERT_EQ(useFormsDesign, System::IO::File::ReadAllText(get_ArtifactsDir() + u"ViewOptions.FormsDesign.xml").Contains(u"<w:formsDesign />"));
```

## انظر أيضًا

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
