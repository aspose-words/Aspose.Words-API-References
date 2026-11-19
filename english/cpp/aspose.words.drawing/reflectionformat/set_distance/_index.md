---
title: Aspose::Words::Drawing::ReflectionFormat::set_Distance method
linktitle: set_Distance
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ReflectionFormat::set_Distance method. Sets a double value that specifies the amount of separation of the reflected image from the object in points. The default value is 0.0 in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.drawing/reflectionformat/set_distance/
---
## ReflectionFormat::set_Distance method


Sets a double value that specifies the amount of separation of the reflected image from the object in points. The default value is 0.0.

```cpp
void Aspose::Words::Drawing::ReflectionFormat::set_Distance(double value)
```

## Examples


Shows how to interact with reflection shape effect.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Various shapes.docx"));
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(NodeType::Shape, 0, true));

shape->get_Reflection()->set_Transparency(0.37);
shape->get_Reflection()->set_Size(0.48);
shape->get_Reflection()->set_Blur(17.5);
shape->get_Reflection()->set_Distance(9.2);

doc->Save(get_ArtifactsDir() + u"Shape.Reflection.docx");

doc = System::MakeObject<Aspose::Words::Document>(System::String(get_ArtifactsDir() + u"Shape.Reflection.docx"));
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::ReflectionFormat> reflectionFormat = shape->get_Reflection();

ASSERT_NEAR(reflectionFormat->get_Transparency(), 0.37, 0.01);
ASSERT_NEAR(reflectionFormat->get_Size(), 0.48, 0.01);
ASSERT_NEAR(reflectionFormat->get_Blur(), 17.5, 0.01);
ASSERT_NEAR(reflectionFormat->get_Distance(), 9.2, 0.01);

reflectionFormat->Remove();

ASPOSE_ASSERT_EQ(reflectionFormat->get_Transparency(), 0);
ASPOSE_ASSERT_EQ(reflectionFormat->get_Size(), 0);
ASPOSE_ASSERT_EQ(reflectionFormat->get_Blur(), 0);
ASPOSE_ASSERT_EQ(reflectionFormat->get_Distance(), 0);
```
## See Also

* [get_Distance](../get_distance/)

* Class [ReflectionFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
