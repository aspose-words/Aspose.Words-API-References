---
title: "Aspose::Words::Drawing::SoftEdgeFormat class"
linktitle: "SoftEdgeFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::SoftEdgeFormat class. Rappresenta la formattazione del bordo morbido per un oggetto in C++."
type: docs
weight: 13500
url: /it/cpp/aspose.words.drawing/softedgeformat/
---
## SoftEdgeFormat class


Rappresenta la formattazione dei bordi morbidi per un oggetto.

```cpp
class SoftEdgeFormat : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Radius](./get_radius/)() | Ottiene o imposta un valore double che rappresenta la lunghezza del raggio per un effetto di bordo morbido in punti (pt). Il valore predefinito è 0,0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Rimuove [SoftEdgeFormat](./) dall'oggetto genitore. |
| [set_Radius](./set_radius/)(double) | Setter per [Aspose::Words::Drawing::SoftEdgeFormat::get_Radius](./get_radius/). |
| static [Type](./type/)() |  |
## Note


Usa la proprietà [SoftEdge](../shapebase/get_softedge/) per accedere alle proprietà del bordo morbido di un oggetto. Non crei istanze della classe [SoftEdgeFormat](./) direttamente.

## Esempi



Mostra come lavorare con la formattazione del bordo morbido.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 200);

// Applica il bordo morbido alla forma.
shape->get_SoftEdge()->set_Radius(30);

builder->get_Document()->Save(get_ArtifactsDir() + u"Shape.SoftEdge.docx");

// Carica un documento con una forma rettangolare con bordo morbido.
auto doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.SoftEdge.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::SoftEdgeFormat> softEdgeFormat = shape->get_SoftEdge();

// Verifica il raggio del bordo morbido.
ASPOSE_ASSERT_EQ(30, softEdgeFormat->get_Radius());

// Rimuovi il bordo morbido dalla forma.
softEdgeFormat->Remove();

// Verifica il raggio del bordo morbido rimosso.
ASPOSE_ASSERT_EQ(0, softEdgeFormat->get_Radius());
```

## Vedi anche

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
