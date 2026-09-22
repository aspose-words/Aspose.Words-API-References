---
title: "طريقة Aspose::Words::Drawing::ReflectionFormat::get_Size"
linktitle: "get_Size"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ReflectionFormat::get_Size. يحصل على أو يضبط قيمة مزدوجة بين 0.0 و 1.0 تمثل حجم الانعكاس كنسبة مئوية من الكائن المنعكس. القيمة الافتراضية هي 0.0 في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.drawing/reflectionformat/get_size/
---
## ReflectionFormat::get_Size method


يحصل أو يعيّن قيمة مزدوجة بين 0.0 و 1.0 تمثل حجم الانعكاس كنسبة مئوية من الكائن المنعكس. القيمة الافتراضية هي 0.0.

```cpp
double Aspose::Words::Drawing::ReflectionFormat::get_Size()
```


## أمثلة



يظهر كيفية التفاعل مع تأثير شكل الانعكاس.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

shape->get_Reflection()->set_Transparency(0.37);
shape->get_Reflection()->set_Size(0.48);
shape->get_Reflection()->set_Blur(17.5);
shape->get_Reflection()->set_Distance(9.2);

doc->Save(get_ArtifactsDir() + u"Shape.Reflection.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Reflection.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::ReflectionFormat> reflectionFormat = shape->get_Reflection();

ASSERT_NEAR(0.37, reflectionFormat->get_Transparency(), 0.01);
ASSERT_NEAR(0.48, reflectionFormat->get_Size(), 0.01);
ASSERT_NEAR(17.5, reflectionFormat->get_Blur(), 0.01);
ASSERT_NEAR(9.2, reflectionFormat->get_Distance(), 0.01);

reflectionFormat->Remove();

ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Transparency());
ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Size());
ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Blur());
ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Distance());
```

## انظر أيضًا

* Class [ReflectionFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
