---
title: "Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked method"
linktitle: "get_AspectRatioLocked"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked method. Spécifie si le rapport d'aspect de la forme est verrouillé en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.drawing/shapebase/get_aspectratiolocked/
---
## ShapeBase::get_AspectRatioLocked method


Spécifie si le ratio d'aspect de la forme est verrouillé.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked()
```

## Remarques


La valeur par défaut dépend du [ShapeType](../../shapetype/), pour le [Image](../../shapetype/) elle est **true** mais pour les autres types de forme elle est **false**.

A un effet uniquement pour les formes de niveau supérieur.

## Exemples



Montre comment verrouiller/déverrouiller le rapport d'aspect d'une forme.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez une forme. Si nous ouvrons ce document dans Microsoft Word, nous pouvons cliquer gauche sur la forme pour révéler
// huit poignées de redimensionnement autour de son périmètre, que nous pouvons cliquer et faire glisser pour modifier sa taille.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Définissez la propriété "AspectRatioLocked" sur "true" pour préserver le rapport d'aspect de la forme
// lors de l'utilisation de l'une des quatre poignées de redimensionnement diagonales, qui modifient à la fois la hauteur et la largeur de l'image.
// Utiliser n'importe quelle poignée de redimensionnement orthogonale qui modifie soit la hauteur soit la largeur modifiera toujours le rapport d'aspect.
// Définissez la propriété "AspectRatioLocked" sur "false" pour nous permettre de
// modifier librement le rapport d'aspect de l'image avec toutes les poignées de redimensionnement.
shape->set_AspectRatioLocked(lockAspectRatio);

doc->Save(get_ArtifactsDir() + u"Shape.AspectRatio.docx");
```

## Voir aussi

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
