---
title: "Aspose::Words::Drawing::GlowFormat class"
linktitle: "GlowFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::GlowFormat-klass. Representerar glödeformatering för ett objekt i C++."
type: docs
weight: 1500
url: /sv/cpp/aspose.words.drawing/glowformat/
---
## GlowFormat class


Representerar glödformatering för ett objekt.

```cpp
class GlowFormat : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Color](./get_color/)() | Hämtar eller anger ett **Color**-objekt som representerar färgen för en glödeffekt. Standardvärdet är **Black**. |
| [get_Radius](./get_radius/)() | Hämtar eller anger ett double‑värde som representerar radie‑längden för en glödeffekt i punkter (pt). Standardvärdet är 0.0. |
| [get_Transparency](./get_transparency/)() | Hämtar eller anger graden av transparens för glödeffekten som ett värde mellan 0.0 (opak) och 1.0 (klar). Standardvärdet är 0.0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Tar bort [GlowFormat](./) från föräldraobjektet. |
| [set_Color](./set_color/)(System::Drawing::Color) | Sättare för [Aspose::Words::Drawing::GlowFormat::get_Color](./get_color/). |
| [set_Radius](./set_radius/)(double) | Sättare för [Aspose::Words::Drawing::GlowFormat::get_Radius](./get_radius/). |
| [set_Transparency](./set_transparency/)(double) | Sättare för [Aspose::Words::Drawing::GlowFormat::get_Transparency](./get_transparency/). |
| static [Type](./type/)() |  |
## Anmärkningar


Använd egenskapen [Glow](../shapebase/get_glow/) för att komma åt glödegenskaper för ett objekt. Du skapar inte instanser av klassen [GlowFormat](./) direkt.

## Exempel



Visar hur man interagerar med glödeffekten för en form.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

shape->get_Glow()->set_Color(System::Drawing::Color::get_Salmon());
shape->get_Glow()->set_Radius(30);
shape->get_Glow()->set_Transparency(0.15);

doc->Save(get_ArtifactsDir() + u"Shape.Glow.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Glow.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(System::Drawing::Color::FromArgb(217, 250, 128, 114).ToArgb(), shape->get_Glow()->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(30, shape->get_Glow()->get_Radius());
ASSERT_NEAR(0.15, shape->get_Glow()->get_Transparency(), 0.01);

shape->get_Glow()->Remove();

ASSERT_EQ(System::Drawing::Color::get_Black().ToArgb(), shape->get_Glow()->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0, shape->get_Glow()->get_Radius());
ASPOSE_ASSERT_EQ(0, shape->get_Glow()->get_Transparency());
```

## Se även

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
