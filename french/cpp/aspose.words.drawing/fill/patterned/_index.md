---
title: "Aspose::Words::Drawing::Fill::Patterned méthode"
linktitle: "Motifé"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Fill::Patterned méthode. Définit le remplissage spécifié à un motif en C++."
type: docs
weight: 26000
url: /fr/cpp/aspose.words.drawing/fill/patterned/
---
## Fill::Patterned(Aspose::Words::Drawing::PatternType) method


Définit le remplissage spécifié à un motif.

```cpp
void Aspose::Words::Drawing::Fill::Patterned(Aspose::Words::Drawing::PatternType patternType)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| patternType | Aspose::Words::Drawing::PatternType | [PatternType](../../patterntype/) |

## Exemples



Montre comment définir un motif pour une forme.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();

std::cout << System::String::Format(u"Pattern value is: {0}", fill->get_Pattern()) << std::endl;

// Il existe plusieurs façons de spécifier le remplissage avec un motif.
// 1 -  Appliquer le motif au remplissage de la forme:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick);

// 2 -  Appliquer le motif avec les couleurs de premier plan et d'arrière-plan au remplissage de la forme:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick, System::Drawing::Color::get_Aqua(), System::Drawing::Color::get_Bisque());

doc->Save(get_ArtifactsDir() + u"Shape.FillPattern.docx");
```

## Voir aussi

* Enum [PatternType](../../patterntype/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## Fill::Patterned(Aspose::Words::Drawing::PatternType, System::Drawing::Color, System::Drawing::Color) method


Définit le remplissage spécifié à un motif.

```cpp
void Aspose::Words::Drawing::Fill::Patterned(Aspose::Words::Drawing::PatternType patternType, System::Drawing::Color foreColor, System::Drawing::Color backColor)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| patternType | Aspose::Words::Drawing::PatternType | [PatternType](../../patterntype/) |
| foreColor | System::Drawing::Color | La couleur du remplissage de premier plan. |
| backColor | System::Drawing::Color | La couleur du remplissage d'arrière-plan. |

## Exemples



Montre comment définir un motif pour une forme.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();

std::cout << System::String::Format(u"Pattern value is: {0}", fill->get_Pattern()) << std::endl;

// Il existe plusieurs façons de spécifier le remplissage avec un motif.
// 1 -  Appliquer le motif au remplissage de la forme:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick);

// 2 -  Appliquer le motif avec les couleurs de premier plan et d'arrière-plan au remplissage de la forme:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick, System::Drawing::Color::get_Aqua(), System::Drawing::Color::get_Bisque());

doc->Save(get_ArtifactsDir() + u"Shape.FillPattern.docx");
```

## Voir aussi

* Enum [PatternType](../../patterntype/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
