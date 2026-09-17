---
title: "Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition méthode"
linktitle: "get_RelativeVerticalPosition"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition méthode. Spécifie par rapport à quoi la forme est positionnée verticalement en C++."
type: docs
weight: 43000
url: /fr/cpp/aspose.words.drawing/shapebase/get_relativeverticalposition/
---
## ShapeBase::get_RelativeVerticalPosition method


Spécifie par rapport à quoi la forme est positionnée verticalement.

```cpp
Aspose::Words::Drawing::RelativeVerticalPosition Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition()
```

## Remarques


La valeur par défaut est [Paragraph](../../relativeverticalposition/).

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

* Enum [RelativeVerticalPosition](../../relativeverticalposition/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
