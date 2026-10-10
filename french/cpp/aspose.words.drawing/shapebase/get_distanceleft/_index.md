---
title: "Aspose::Words::Drawing::ShapeBase::get_DistanceLeft méthode"
linktitle: "get_DistanceLeft"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_DistanceLeft méthode. Retourne ou définit la distance (en points) entre le texte du document et le bord gauche de la forme en C++."
type: docs
weight: 16000
url: /fr/cpp/aspose.words.drawing/shapebase/get_distanceleft/
---
## ShapeBase::get_DistanceLeft method


Renvoie ou définit la distance (en points) entre le texte du document et le bord gauche de la forme.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_DistanceLeft()
```

## Remarques


La valeur par défaut est 1/8 pouce.

N'a d'effet que pour les formes de niveau supérieur.

## Exemples



Montre comment définir la distance d'habillage pour un texte qui entoure une forme.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez un rectangle et, faites en sorte que le texte s'enroule étroitement autour de ses limites.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 150, 150);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Tight);

// Définissez la distance minimale entre la forme et le texte environnant à 40 pt de tous les côtés.
shape->set_DistanceTop(40);
shape->set_DistanceBottom(40);
shape->set_DistanceLeft(40);
shape->set_DistanceRight(40);

// Déplacez la forme plus près du centre de la page, puis faites pivoter la forme de 60 degrés dans le sens des aiguilles d'une montre.
shape->set_Top(75);
shape->set_Left(150);
shape->set_Rotation(60);

// Ajoutez du texte qui s'enroulera autour de la forme.
builder->get_Font()->set_Size(24);
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc->Save(get_ArtifactsDir() + u"Shape.Coordinates.docx");
```

## Voir aussi

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
