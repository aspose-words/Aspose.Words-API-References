---
title: "Aspose::Words::Drawing::ShapeBase::get_WidthRelative méthode"
linktitle: "get_WidthRelative"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_WidthRelative méthode. Obtient ou définit la valeur qui représente le pourcentage de la largeur relative de la forme en C++."
type: docs
weight: 54500
url: /fr/cpp/aspose.words.drawing/shapebase/get_widthrelative/
---
## ShapeBase::get_WidthRelative method


Obtient ou définit la valeur qui représente le pourcentage de la largeur relative de la forme.

```cpp
float Aspose::Words::Drawing::ShapeBase::get_WidthRelative()
```


## Exemples



Montre comment définir la taille et la position relatives.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ajout d'une forme simple avec une taille et une position absolues.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 40);
// Définissez WrapType sur WrapType.None car les formes Inline sont automatiquement converties en unités absolues.
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Vérification et définition de la taille horizontale relative.
if (shape->get_RelativeHorizontalSize() == Aspose::Words::Drawing::RelativeHorizontalSize::Default)
{
    // Définition de la liaison de la taille horizontale à Margin.
    shape->set_RelativeHorizontalSize(Aspose::Words::Drawing::RelativeHorizontalSize::Margin);
    // Définition de la largeur à 50 % de la largeur de Margin.
    shape->set_WidthRelative(50.0f);
}

// Vérification et définition de la taille verticale relative.
if (shape->get_RelativeVerticalSize() == Aspose::Words::Drawing::RelativeVerticalSize::Default)
{
    // Définition de la liaison de la taille verticale à Margin.
    shape->set_RelativeVerticalSize(Aspose::Words::Drawing::RelativeVerticalSize::Margin);
    // Définition de la hauteur à 30 % de la hauteur de Margin.
    shape->set_HeightRelative(30.0f);
}

// Vérification et définition de la position verticale relative.
if (shape->get_RelativeVerticalPosition() == Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph)
{
    // Définition de la liaison de la position à TopMargin.
    shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin);
    // Définition du Top relatif à 30 % de la position TopMargin.
    shape->set_TopRelative(30.0f);
}

// Vérification et définition de la position horizontale relative.
if (shape->get_RelativeHorizontalPosition() == Aspose::Words::Drawing::RelativeHorizontalPosition::Default)
{
    // Définition de la liaison de la position à RightMargin.
    shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin);
    // La valeur relative de la position peut être négative.
    shape->set_LeftRelative(-260.0f);
}

doc->Save(get_ArtifactsDir() + u"Shape.RelativeSizeAndPosition.docx");
```

## Voir aussi

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
