---
title: "Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment méthode"
linktitle: "get_HorizontalAlignment"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment méthode. Spécifie comment la forme est positionnée horizontalement en C++."
type: docs
weight: 23000
url: /fr/cpp/aspose.words.drawing/shapebase/get_horizontalalignment/
---
## ShapeBase::get_HorizontalAlignment method


Spécifie comment la forme est positionnée horizontalement.

```cpp
Aspose::Words::Drawing::HorizontalAlignment Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment()
```

## Remarques


La valeur par défaut est [None](../../horizontalalignment/).

N'a d'effet que pour les formes flottantes de niveau supérieur.

## Exemples



Montre comment insérer une image flottante au centre d'une page.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez une image flottante qui apparaîtra derrière le texte qui se chevauche et alignez‑la au centre de la page.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## Voir aussi

* Enum [HorizontalAlignment](../../horizontalalignment/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
