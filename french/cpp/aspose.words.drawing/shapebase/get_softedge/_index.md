---
title: "Aspose::Words::Drawing::ShapeBase::get_SoftEdge méthode"
linktitle: "get_SoftEdge"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_SoftEdge méthode. Obtient le formatage des bords doux pour la forme en C++."
type: docs
weight: 49500
url: /fr/cpp/aspose.words.drawing/shapebase/get_softedge/
---
## ShapeBase::get_SoftEdge method


Obtient le format de bord doux pour la forme.

```cpp
System::SharedPtr<Aspose::Words::Drawing::SoftEdgeFormat> Aspose::Words::Drawing::ShapeBase::get_SoftEdge()
```


## Exemples



Montre comment travailler avec le formatage à bord doux.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 200);

// Appliquez le bord doux à la forme.
shape->get_SoftEdge()->set_Radius(30);

builder->get_Document()->Save(get_ArtifactsDir() + u"Shape.SoftEdge.docx");

// Chargez le document avec une forme rectangulaire à bord doux.
auto doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.SoftEdge.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::SoftEdgeFormat> softEdgeFormat = shape->get_SoftEdge();

// Vérifiez le rayon du bord doux.
ASPOSE_ASSERT_EQ(30, softEdgeFormat->get_Radius());

// Supprimer le bord doux de la forme.
softEdgeFormat->Remove();

// Vérifier le rayon du bord doux supprimé.
ASPOSE_ASSERT_EQ(0, softEdgeFormat->get_Radius());
```


Montre comment définir une limite pour la résolution des images.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_MaxImageResolution(72);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

## Voir aussi

* Class [SoftEdgeFormat](../../softedgeformat/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
