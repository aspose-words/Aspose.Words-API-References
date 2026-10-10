---
title: "Aspose::Words::Drawing::ShapeBase::get_BehindText méthode"
linktitle: "get_BehindText"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_BehindText méthode. Spécifie si la forme est en dessous ou au-dessus du texte en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.drawing/shapebase/get_behindtext/
---
## ShapeBase::get_BehindText method


Spécifie si la forme est en dessous ou au-dessus du texte.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_BehindText()
```

## Remarques


N'a d'effet que pour les formes de niveau supérieur.

La valeur par défaut est **false**.

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

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
