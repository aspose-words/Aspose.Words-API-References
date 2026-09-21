---
title: "Aspose::Words::Drawing::ShapeBase::get_Fill metod"
linktitle: "get_Fill"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_Fill metod. Hämtar fyllningsformat för formen i C++."
type: docs
weight: 19000
url: /sv/cpp/aspose.words.drawing/shapebase/get_fill/
---
## ShapeBase::get_Fill method


Hämtar fyllningsformatering för formen.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Fill> Aspose::Words::Drawing::ShapeBase::get_Fill()
```


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

* Class [Fill](../../fill/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
