---
title: "Aspose::Words::Drawing::ReflectionFormat::get_Transparency metod"
linktitle: "get_Transparency"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ReflectionFormat::get_Transparency metod. Hämtar eller anger ett double‑värde mellan 0.0 (opak) och 1.0 (klar) som representerar graden av transparens för reflektionseffekten. Standardvärdet är 0.0 i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.drawing/reflectionformat/get_transparency/
---
## ReflectionFormat::get_Transparency method


Hämtar eller anger ett dubbelvärde mellan 0.0 (opak) och 1.0 (klar) som representerar graden av transparens för reflektionseffekten. Standardvärdet är 0.0.

```cpp
double Aspose::Words::Drawing::ReflectionFormat::get_Transparency()
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
