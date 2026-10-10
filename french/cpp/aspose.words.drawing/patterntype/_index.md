---
title: "Aspose::Words::Drawing::PatternType enum"
linktitle: "PatternType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::PatternType enum. Spécifie le motif de remplissage à utiliser pour remplir une forme en C++."
type: docs
weight: 31000
url: /fr/cpp/aspose.words.drawing/patterntype/
---
## PatternType enum


Spécifie le motif de remplissage à utiliser pour remplir une forme.

```cpp
enum class PatternType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | -1 | Aucun motif. |
| Percent10 | 1 | 10 % de la couleur de premier plan. |
| Percent20 | 2 | 20 % de la couleur de premier plan. |
| Percent25 | 3 | 25 % de la couleur de premier plan. |
| Percent30 | 4 | 30 % de la couleur de premier plan. |
| Percent40 | 5 | 40 % de la couleur de premier plan |
| Percent50 | 6 | 50 % de la couleur de premier plan |
| Percent5 | 7 | 5 % de la couleur de premier plan. |
| Percent60 | 8 | 60 % de la couleur de premier plan. |
| Percent70 | 9 | 70 % de la couleur de premier plan. |
| Percent75 | 10 | 75 % de la couleur de premier plan. |
| Percent80 | 11 | 80 % de la couleur de premier plan. |
| Percent90 | 12 | 90 % de la couleur de premier plan. |
| Croix | 13 | Croix. |
| DiagonaleDescendanteSombre | 14 | Diagonale descendante sombre. |
| HorizontaleSombre | 15 | Horizontale sombre. |
| DiagonaleMontanteSombre | 16 | Diagonale montante sombre. |
| VerticaleSombre | 17 | Verticale sombre. |
| DiagonaleDescendantePointillée | 18 | Diagonale descendante pointillée. |
| HorizontalePointillée | 19 | Horizontale pointillée. |
| DiagonaleMontantePointillée | 20 | Diagonale montante pointillée. |
| VerticalePointillée | 21 | Verticale pointillée. |
| BriqueDiagonale | 22 | Brique diagonale. |
| CroixDiagonale | 23 | Croix diagonale. |
| Creux | 24 | Motif creux. |
| DiamantPointillé | 25 | Diamant pointillé. |
| DottedGrid | 26 | Grille pointillée. |
| DownwardDiagonal | 27 | Diagonale descendante. |
| Horizontal | 28 | Horizontal. |
| HorizontalBrick | 29 | Brique horizontale. |
| LargeCheckerBoard | 30 | Grand damier. |
| LargeConfetti | 31 | Grand confettis. |
| LargeGrid | 32 | Grande grille. |
| LightDownwardDiagonal | 33 | Diagonale descendante claire. |
| LightHorizontal | 34 | Horizontal clair. |
| LightUpwardDiagonal | 36 | Diagonale ascendante claire. |
| LightVertical | 37 | Vertical clair. |
| NarrowHorizontal | 38 | Horizontal étroit. |
| NarrowVertical | 39 | Vertical étroit. |
| OutlinedDiamond | 40 | Losange contouré. |
| Plaid | 41 | Carreau. |
| Shingle | 42 | Bardeau. |
| SmallCheckerBoard | 43 | Petit damier. |
| SmallConfetti | 44 | Petits confettis. |
| SmallGrid | 45 | Petite grille. |
| SolidDiamond | 46 | Losange plein. |
| Sphere | 47 | Sphère. |
| Trellis | 48 | Treillis. |
| UpwardDiagonal | 49 | Diagonale ascendante. |
| Vertical | 50 | Vertical. |
| Wave | 51 | Vague. |
| Weave | 52 | Tissage. |
| WideDownwardDiagonal | 53 | Large diagonale descendante. |
| WideUpwardDiagonal | 54 | Diagonale ascendante large. |
| ZigZag | 55 | Zigzag. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
