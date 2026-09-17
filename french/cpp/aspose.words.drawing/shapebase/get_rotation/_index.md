---
title: "Aspose::Words::Drawing::ShapeBase::get_Rotation method"
linktitle: "get_Rotation"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_Rotation method. Définit l'angle (en degrés) selon lequel une forme est tournée. Une valeur positive correspond à un angle de rotation horaire en C++."
type: docs
weight: 45000
url: /fr/cpp/aspose.words.drawing/shapebase/get_rotation/
---
## ShapeBase::get_Rotation method


Définit l'angle (en degrés) auquel une forme est tournée. Une valeur positive correspond à un angle de rotation horaire.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Rotation()
```

## Remarques


La valeur par défaut est 0.

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
