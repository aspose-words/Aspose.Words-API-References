---
title: "Aspose::Words::Drawing::Shape::get_FillColor metod"
linktitle: "get_FillColor"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Shape::get_FillColor metod. Definierar penselfärgen som fyller den slutna banan av formen i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.drawing/shape/get_fillcolor/
---
## Shape::get_FillColor method


Definierar penselfärgen som fyller den slutna banan för formen.

```cpp
System::Drawing::Color Aspose::Words::Drawing::Shape::get_FillColor()
```

## Anmärkningar


Detta är en genväg till egenskapen [Color](../../fill/get_color/).

Standardvärdet är **White**.

## Exempel



Visar hur man fyller en form med en solid färg.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skriv lite text och täck sedan den med en flytande form.
builder->get_Font()->set_Size(32);
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::CloudCallout, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 25, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 25, 250, 150, Aspose::Words::Drawing::WrapType::None);

// Använd egenskapen "StrokeColor" för att ange färgen på formens kontur.
shape->set_StrokeColor(System::Drawing::Color::get_CadetBlue());

// Använd egenskapen "FillColor" för att ange färgen på formens inneryta.
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

// Egenskapen "Opacity" bestämmer hur genomskinlig färgen är på en skala från 0 till 1,
// där 1 är helt ogenomskinlig och 0 är osynlig.
// Formens fyllning är som standard helt ogenomskinlig, så vi kan inte se texten som den ligger ovanpå.
ASPOSE_ASSERT_EQ(1.0, shape->get_Fill()->get_Opacity());

// Sätt formens fyllningsfärgs opacitet till ett lägre värde så att vi kan se texten under den.
shape->get_Fill()->set_Opacity(0.3);

doc->Save(get_ArtifactsDir() + u"Shape.Fill.docx");
```

## Se även

* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
