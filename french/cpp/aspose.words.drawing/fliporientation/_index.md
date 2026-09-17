---
title: "Aspose::Words::Drawing::FlipOrientation enum"
linktitle: "FlipOrientation"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::FlipOrientation enum. Valeurs possibles pour l'orientation d'une forme en C++."
type: docs
weight: 23000
url: /fr/cpp/aspose.words.drawing/fliporientation/
---
## FlipOrientation enum


Valeurs possibles pour l'orientation d'une forme.

```cpp
enum class FlipOrientation
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 | Les coordonnées ne sont pas inversées. |
| Horizontal | 1 | Retourner le long de l'axe y, en inversant les coordonnées x. |
| Vertical | 2 | Retourner le long de l'axe x, en inversant les coordonnées y. |
| Both | 3 | Retourner le long des axes y et x. |


## Exemples



Montre comment retourner une forme sur un axe.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez une forme d'image et laissez son orientation dans son état par défaut.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

ASSERT_EQ(Aspose::Words::Drawing::FlipOrientation::None, shape->get_FlipOrientation());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 250, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Définissez la propriété "FlipOrientation" sur "FlipOrientation.Horizontal" pour retourner la deuxième forme sur l'axe y,
// la transformant en une image miroir horizontale de la première forme.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Horizontal);

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 250, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Définissez la propriété "FlipOrientation" sur "FlipOrientation.Horizontal" pour retourner la troisième forme sur l'axe x,
// la transformant en une image miroir verticale de la première forme.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Vertical);

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 250, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 250, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Définissez la propriété "FlipOrientation" sur "FlipOrientation.Horizontal" pour retourner la quatrième forme sur les axes x et y,
// la transformant en une image miroir horizontale et verticale de la première forme.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Both);

doc->Save(get_ArtifactsDir() + u"Shape.FlipShapeOrientation.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
