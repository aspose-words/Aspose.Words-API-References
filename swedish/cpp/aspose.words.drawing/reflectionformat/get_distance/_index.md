---
title: "Aspose::Words::Drawing::ReflectionFormat::get_Distance metod"
linktitle: "get_Distance"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ReflectionFormat::get_Distance metod. Hämtar eller anger ett dubbelvärde som specificerar mängden avstånd mellan den reflekterade bilden och objektet i punkter. Standardvärdet är 0,0 i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.drawing/reflectionformat/get_distance/
---
## ReflectionFormat::get_Distance method


Hämtar eller anger ett dubbelvärde som specificerar mängden avstånd mellan den reflekterade bilden och objektet i punkter. Standardvärdet är 0.0.

```cpp
double Aspose::Words::Drawing::ReflectionFormat::get_Distance()
```


## Exempel



Visar hur man interagerar med reflektionseffekten för en form.
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

## Se även

* Class [ReflectionFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
