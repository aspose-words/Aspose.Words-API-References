---
title: "Aspose::Words::Drawing::ShapeBase::get_CanHaveImage méthode"
linktitle: "get_CanHaveImage"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_CanHaveImage méthode. Retourne **true** si le type de forme permet à la forme d’avoir une image en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words.drawing/shapebase/get_canhaveimage/
---
## ShapeBase::get_CanHaveImage method


Renvoie **true** si le type de forme autorise la forme à contenir une image.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_CanHaveImage()
```

## Remarques


Bien que Microsoft Word dispose d’un type de forme spécial pour les images, il semble que dans les documents Microsoft Word toute forme, à l’exception d’une forme de groupe, puisse contenir une image ; par conséquent, cette propriété renvoie **true** pour toutes les formes sauf [GroupShape](../../groupshape/).

## Exemples



Montre comment insérer et faire pivoter une image.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérer une forme avec une image.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
ASSERT_TRUE(shape->get_CanHaveImage());
ASSERT_TRUE(shape->get_HasImage());

// Faire pivoter l’image de 45 degrés dans le sens des aiguilles d’une montre.
shape->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Shape.Rotate.docx");
```

## Voir aussi

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
