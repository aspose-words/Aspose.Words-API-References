---
title: "Aspose::Words::Drawing::SoftEdgeFormat class"
linktitle: "SoftEdgeFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::SoftEdgeFormat class. Représente le formatage à bord doux pour un objet en C++."
type: docs
weight: 13500
url: /fr/cpp/aspose.words.drawing/softedgeformat/
---
## SoftEdgeFormat class


Représente le format de bord doux d'un objet.

```cpp
class SoftEdgeFormat : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Radius](./get_radius/)() | Obtient ou définit une valeur double qui représente la longueur du rayon pour un effet à bord doux en points (pt). La valeur par défaut est 0,0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Supprime [SoftEdgeFormat](./) de l'objet parent. |
| [set_Radius](./set_radius/)(double) | Définisseur pour [Aspose::Words::Drawing::SoftEdgeFormat::get_Radius](./get_radius/). |
| static [Type](./type/)() |  |
## Remarques


Utilisez la propriété [SoftEdge](../shapebase/get_softedge/) pour accéder aux propriétés de bord doux d'un objet. Vous ne créez pas d'instances de la classe [SoftEdgeFormat](./) directement.

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

## Voir aussi

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
