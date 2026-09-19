---
title: "Aspose::Words::Drawing::ShapeBase::get_SoftEdge metodo"
linktitle: "get_SoftEdge"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShapeBase::get_SoftEdge metodo. Restituisce la formattazione del bordo morbido per la forma in C++."
type: docs
weight: 49500
url: /it/cpp/aspose.words.drawing/shapebase/get_softedge/
---
## ShapeBase::get_SoftEdge method


Ottiene la formattazione del bordo morbido per la forma.

```cpp
System::SharedPtr<Aspose::Words::Drawing::SoftEdgeFormat> Aspose::Words::Drawing::ShapeBase::get_SoftEdge()
```


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


Mostra come impostare il limite per la risoluzione delle immagini.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_MaxImageResolution(72);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

## Vedi anche

* Class [SoftEdgeFormat](../../softedgeformat/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
