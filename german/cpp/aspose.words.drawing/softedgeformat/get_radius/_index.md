---
title: "Aspose::Words::Drawing::SoftEdgeFormat::get_Radius Methode"
linktitle: "get_Radius"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::SoftEdgeFormat::get_Radius Methode. Ruft einen double-Wert ab oder legt ihn fest, der die Länge des Radius für einen Soft-Edge-Effekt in Punkten (pt) darstellt. Der Standardwert ist 0.0 in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.drawing/softedgeformat/get_radius/
---
## SoftEdgeFormat::get_Radius method


Liest oder setzt einen double-Wert, der die Länge des Radius für einen Weichkanten-Effekt in Punkten (pt) darstellt. Der Standardwert ist 0,0.

```cpp
double Aspose::Words::Drawing::SoftEdgeFormat::get_Radius()
```


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


Zeigt, wie man das Limit für die Bildauflösung festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_MaxImageResolution(72);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

## Siehe auch

* Class [SoftEdgeFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
