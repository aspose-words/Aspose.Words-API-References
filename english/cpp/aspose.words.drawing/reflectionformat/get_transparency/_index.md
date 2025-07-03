---
title: Aspose::Words::Drawing::ReflectionFormat::get_Transparency method
linktitle: get_Transparency
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ReflectionFormat::get_Transparency method. Gets or sets a double value between 0.0 (opaque) and 1.0 (clear) representing the degree of transparency for the reflection effect. The default value is 0.0 in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.drawing/reflectionformat/get_transparency/
---
## ReflectionFormat::get_Transparency method


Gets or sets a double value between 0.0 (opaque) and 1.0 (clear) representing the degree of transparency for the reflection effect. The default value is 0.0.

```cpp
double Aspose::Words::Drawing::ReflectionFormat::get_Transparency()
```


## Examples



Shows how to interact with reflection shape effect. 
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

## See Also

* Class [ReflectionFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
