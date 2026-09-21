---
title: "Aspose::Words::Drawing::ReflectionFormat klass"
linktitle: "ReflectionFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ReflectionFormat klass. Representerar reflektionens formatering för ett objekt i C++."
type: docs
weight: 9500
url: /sv/cpp/aspose.words.drawing/reflectionformat/
---
## ReflectionFormat class


Representerar reflektionens formatering för ett objekt.

```cpp
class ReflectionFormat : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Blur](./get_blur/)() | Hämtar eller anger ett dubbelvärde som specificerar graden av oskärpeeffekt som tillämpas på reflektionseffekten i punkter. Standardvärdet är 0.0. |
| [get_Distance](./get_distance/)() | Hämtar eller anger ett dubbelvärde som specificerar mängden avstånd mellan den reflekterade bilden och objektet i punkter. Standardvärdet är 0.0. |
| [get_Size](./get_size/)() | Hämtar eller anger ett dubbelvärde mellan 0.0 och 1.0 som representerar storleken på reflektionen som en procentandel av det reflekterade objektet. Standardvärdet är 0.0. |
| [get_Transparency](./get_transparency/)() | Hämtar eller anger ett dubbelvärde mellan 0.0 (opak) och 1.0 (klar) som representerar graden av transparens för reflektionseffekten. Standardvärdet är 0.0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Tar bort [ReflectionFormat](./) från föräldraobjektet. |
| [set_Blur](./set_blur/)(double) | Sättare för [Aspose::Words::Drawing::ReflectionFormat::get_Blur](./get_blur/). |
| [set_Distance](./set_distance/)(double) | Sättare för [Aspose::Words::Drawing::ReflectionFormat::get_Distance](./get_distance/). |
| [set_Size](./set_size/)(double) | Sättare för [Aspose::Words::Drawing::ReflectionFormat::get_Size](./get_size/). |
| [set_Transparency](./set_transparency/)(double) | Sättare för [Aspose::Words::Drawing::ReflectionFormat::get_Transparency](./get_transparency/). |
| static [Type](./type/)() |  |
## Anmärkningar


Använd egenskapen [Reflection](../shapebase/get_reflection/) för att komma åt reflektionsegenskaper för ett objekt. Du skapar inte instanser av klassen [ReflectionFormat](./) direkt.

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
