---
title: "Aspose::Words::Drawing::SoftEdgeFormat class"
linktitle: "SoftEdgeFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::SoftEdgeFormat class. Representerar mjuk kantformatering för ett objekt i C++."
type: docs
weight: 13500
url: /sv/cpp/aspose.words.drawing/softedgeformat/
---
## SoftEdgeFormat class


Representerar mjuk kant‑formatering för ett objekt.

```cpp
class SoftEdgeFormat : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Radius](./get_radius/)() | Hämtar eller anger ett dubbelvärde som representerar längden på radien för en mjuk kant-effekt i punkter (pt). Standardvärdet är 0,0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Tar bort [SoftEdgeFormat](./) från föräldraobjektet. |
| [set_Radius](./set_radius/)(double) | Sättare för [Aspose::Words::Drawing::SoftEdgeFormat::get_Radius](./get_radius/). |
| static [Type](./type/)() |  |
## Anmärkningar


Använd egenskapen [SoftEdge](../shapebase/get_softedge/) för att komma åt mjuka kant-egenskaper för ett objekt. Du skapar inte instanser av klassen [SoftEdgeFormat](./) direkt.

## Exempel



Visar hur man arbetar med mjuk kantformatering.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 200);

// Applicera mjuk kant på formen.
shape->get_SoftEdge()->set_Radius(30);

builder->get_Document()->Save(get_ArtifactsDir() + u"Shape.SoftEdge.docx");

// Läs in dokument med rektangelform med mjuk kant.
auto doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.SoftEdge.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::SoftEdgeFormat> softEdgeFormat = shape->get_SoftEdge();

// Kontrollera radien för mjuk kant.
ASPOSE_ASSERT_EQ(30, softEdgeFormat->get_Radius());

// Ta bort mjuk kant från formen.
softEdgeFormat->Remove();

// Kontrollera radien för den borttagna mjuka kanten.
ASPOSE_ASSERT_EQ(0, softEdgeFormat->get_Radius());
```

## Se även

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
