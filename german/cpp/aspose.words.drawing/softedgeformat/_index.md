---
title: "Aspose::Words::Drawing::SoftEdgeFormat Klasse"
linktitle: "SoftEdgeFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::SoftEdgeFormat Klasse. Stellt die Weichkantformatierung für ein Objekt in C++ dar."
type: docs
weight: 13500
url: /de/cpp/aspose.words.drawing/softedgeformat/
---
## SoftEdgeFormat class


Stellt die Weichkant-Formatierung für ein Objekt dar.

```cpp
class SoftEdgeFormat : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Radius](./get_radius/)() | Liest oder setzt einen double-Wert, der die Länge des Radius für einen Weichkanten-Effekt in Punkten (pt) darstellt. Der Standardwert ist 0,0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Entfernt [SoftEdgeFormat](./) aus dem übergeordneten Objekt. |
| [set_Radius](./set_radius/)(double) | Setter für [Aspose::Words::Drawing::SoftEdgeFormat::get_Radius](./get_radius/). |
| static [Type](./type/)() |  |
## Hinweise


Verwenden Sie die Eigenschaft [SoftEdge](../shapebase/get_softedge/), um auf die Weichkanten-Eigenschaften eines Objekts zuzugreifen. Sie erstellen keine Instanzen der Klasse [SoftEdgeFormat](./) direkt.

## Beispiele



Zeigt, wie man mit Weichkantenformatierung arbeitet.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 200);

// Weichkante auf die Form anwenden.
shape->get_SoftEdge()->set_Radius(30);

builder->get_Document()->Save(get_ArtifactsDir() + u"Shape.SoftEdge.docx");

// Laden Sie ein Dokument mit einer Rechteckform mit Weichkante.
auto doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.SoftEdge.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::SoftEdgeFormat> softEdgeFormat = shape->get_SoftEdge();

// Weichkantenradius prüfen.
ASPOSE_ASSERT_EQ(30, softEdgeFormat->get_Radius());

// Weichkante aus der Form entfernen.
softEdgeFormat->Remove();

// Radius der entfernten Weichkante prüfen.
ASPOSE_ASSERT_EQ(0, softEdgeFormat->get_Radius());
```

## Siehe auch

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
