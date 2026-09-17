---
title: "Aspose::Words::DocumentBuilder::InsertShape méthode"
linktitle: "InsertShape"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::InsertShape méthode. Insère une forme flottante avec une position, une taille et un type d'habillage de texte spécifiés en C++."
type: docs
weight: 45000
url: /fr/cpp/aspose.words/documentbuilder/insertshape/
---
## DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Insère une forme flottante avec la position, la taille et le type d'habillage du texte spécifiés.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType shapeType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| shapeType | Aspose::Words::Drawing::ShapeType | Le type de forme à insérer dans le document |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Spécifie à partir de quel point la distance horizontale jusqu'à la forme est mesurée. |
| left | double | Distance en points depuis l'origine jusqu'au côté gauche de la forme. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Spécifie à partir de quel point la distance verticale par rapport à la forme est mesurée. |
| top | double | Distance en points de l'origine au côté supérieur de la forme. |
| largeur | double | La largeur de la forme en points. |
| hauteur | double | La hauteur de la forme en points. |
| wrapType | Aspose::Words::Drawing::WrapType | Spécifie comment envelopper le texte autour de la forme. |

### ReturnValue

Le nœud de forme qui a été inséré.

## Exemples



Montre comment insérer des formes DML dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Voici deux types d'habillage que les formes peuvent avoir.
// 1 -  Flottant :
builder->InsertShape(Aspose::Words::Drawing::ShapeType::TopCornersRounded, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 100, 50, 50, Aspose::Words::Drawing::WrapType::None);

// 2 -  En ligne :
builder->InsertShape(Aspose::Words::Drawing::ShapeType::DiagonalCornersRounded, 50, 50);

// Si vous devez créer des formes "non-primitive", telles que SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, ou DiagonalCornersRounded,
// alors enregistrez le document avec la conformité "Strict" ou "Transitional", ce qui permet d'enregistrer la forme en tant que DML.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeInsertion.docx", saveOptions);
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType, double, double) method


Insère une forme en ligne avec le type et la taille spécifiés.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType shapeType, double width, double height)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| shapeType | Aspose::Words::Drawing::ShapeType | Le type de forme à insérer dans le document. |
| largeur | double | La largeur de la forme en points. |
| hauteur | double | La hauteur de la forme en points. |

### ReturnValue

Le nœud de forme qui a été inséré.

## Exemples



Montre comment insérer des formes DML dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Voici deux types d'habillage que les formes peuvent avoir.
// 1 -  Flottant :
builder->InsertShape(Aspose::Words::Drawing::ShapeType::TopCornersRounded, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 100, 50, 50, Aspose::Words::Drawing::WrapType::None);

// 2 -  En ligne :
builder->InsertShape(Aspose::Words::Drawing::ShapeType::DiagonalCornersRounded, 50, 50);

// Si vous devez créer des formes "non-primitive", telles que SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, ou DiagonalCornersRounded,
// alors enregistrez le document avec la conformité "Strict" ou "Transitional", ce qui permet d'enregistrer la forme en tant que DML.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeInsertion.docx", saveOptions);
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
