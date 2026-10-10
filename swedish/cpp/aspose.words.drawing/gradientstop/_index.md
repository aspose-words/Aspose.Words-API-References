---
title: "Aspose::Words::Drawing::GradientStop class"
linktitle: "GradientStop"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::GradientStop-klass. Representerar ett gradientstopp. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.drawing/gradientstop/
---
## GradientStop class


Representerar en gradientstopp. För att lära dig mer, besök dokumentationsartikeln [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/).

```cpp
class GradientStop : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_BaseColor](./get_basecolor/)() | Hämtar ett värde som representerar färgen på gradientstoppet utan några modifierare. |
| [get_Color](./get_color/)() | Hämtar eller anger ett värde som representerar färgen på gradientstoppet. |
| [get_Position](./get_position/)() const | Hämtar eller anger ett värde som representerar positionen för ett stopp i gradienten uttryckt som en procentandel i intervallet 0.0 till 1.0. |
| [get_Transparency](./get_transparency/)() const | Hämtar eller anger ett värde som representerar transparensen för gradientfyllningen uttryckt som en procentandel i intervallet 0.0 till 1.0. |
| [GetType](./gettype/)() const override |  |
| [GradientStop](./gradientstop/)(System::Drawing::Color, double) | Initierar en ny instans av klassen [GradientStop](./). |
| [GradientStop](./gradientstop/)(System::Drawing::Color, double, double) | Initierar en ny instans av klassen [GradientStop](./). |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Tar bort gradientstoppet från den överordnade [GradientStopCollection](../gradientstopcollection/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Sättare för [Aspose::Words::Drawing::GradientStop::get_Color](./get_color/). |
| [set_Position](./set_position/)(double) | Sättare för [Aspose::Words::Drawing::GradientStop::get_Position](./get_position/). |
| [set_Transparency](./set_transparency/)(double) | Sättare för [Aspose::Words::Drawing::GradientStop::get_Transparency](./get_transparency/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man lägger till gradientstopp i gradientfyllningen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
shape->get_Fill()->TwoColorGradient(System::Drawing::Color::get_Green(), System::Drawing::Color::get_Red(), Aspose::Words::Drawing::GradientStyle::Horizontal, Aspose::Words::Drawing::GradientVariant::Variant2);

// Hämta samling av gradientstopp.
System::SharedPtr<Aspose::Words::Drawing::GradientStopCollection> gradientStops = shape->get_Fill()->get_GradientStops();

// Ändra första gradientstoppet.
gradientStops->idx_get(0)->set_Color(System::Drawing::Color::get_Aqua());
gradientStops->idx_get(0)->set_Position(0.1);
gradientStops->idx_get(0)->set_Transparency(0.25);

// Lägg till ett nytt gradientstopp i slutet av samlingen.
auto gradientStop = System::MakeObject<Aspose::Words::Drawing::GradientStop>(System::Drawing::Color::get_Brown(), 0.5);
gradientStops->Add(gradientStop);

// Ta bort gradientstopp vid index 1.
gradientStops->RemoveAt(1);
// Och infoga ett nytt gradientstopp på samma index 1.
gradientStops->Insert(1, System::MakeObject<Aspose::Words::Drawing::GradientStop>(System::Drawing::Color::get_Chocolate(), 0.75, 0.3));

// Ta bort sista gradientstoppet i samlingen.
gradientStop = gradientStops->idx_get(2);
gradientStops->Remove(gradientStop);

ASSERT_EQ(2, gradientStops->get_Count());

ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 0, 255, 255), gradientStops->idx_get(0)->get_BaseColor());
ASSERT_EQ(System::Drawing::Color::get_Aqua().ToArgb(), gradientStops->idx_get(0)->get_Color().ToArgb());
ASSERT_NEAR(0.1, gradientStops->idx_get(0)->get_Position(), 0.01);
ASSERT_NEAR(0.25, gradientStops->idx_get(0)->get_Transparency(), 0.01);

ASSERT_EQ(System::Drawing::Color::get_Chocolate().ToArgb(), gradientStops->idx_get(1)->get_Color().ToArgb());
ASSERT_NEAR(0.75, gradientStops->idx_get(1)->get_Position(), 0.01);
ASSERT_NEAR(0.3, gradientStops->idx_get(1)->get_Transparency(), 0.01);

// Använd efterlevnadsalternativet för att definiera formen med DML
// om du vill hämta egenskapen "GradientStops" efter att dokumentet sparats.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientStops.docx", saveOptions);
```

## Se även

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
