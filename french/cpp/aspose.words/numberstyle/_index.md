---
title: "Aspose::Words::NumberStyle enum"
linktitle: "NumberStyle"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::NumberStyle enum. Spécifie le style de numérotation pour une liste, des notes de bas de page et des notes de fin, ainsi que les numéros de page en C++."
type: docs
weight: 103000
url: /fr/cpp/aspose.words/numberstyle/
---
## NumberStyle enum


Spécifie le style de numérotation pour une liste, des notes de bas de page et des notes de fin, les numéros de page.

```cpp
enum class NumberStyle
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Arabe | 0 | Numérotation arabe (1, 2, 3, ...) |
| UppercaseRoman | 1 | Romain majuscule (I, II, III, ...) |
| LowercaseRoman | 2 | Romain minuscule (i, ii, iii, ...) |
| UppercaseLetter | 3 | Lettre majuscule (A, B, C, ...) |
| LowercaseLetter | 4 | Lettre minuscule (a, b, c, ...) |
| Ordinal | 5 | Ordinal (1er, 2e, 3e, ...) |
| Nombre | 6 | Numéroté (Un, Deux, Trois, ...) |
| OrdinalText | 7 | Ordinal (texte) (Premier, Deuxième, Troisième, ...) |
| Hex | 8 | Hexadécimal: 8, 9, A, B, C, D, E, F, 10, 11, 12. |
| ChicagoManual | 9 | Manuel Chicago de [Style](../style/): *, †, † |
| Kanji | 10 | Idéographe-numérique. |
| KanjiDigit | 11 | Comptage japonais. |
| AiueoHalfWidth | 12 | Aiueo. |
| IrohaHalfWidth | 13 | Iroha. |
| ArabicFullWidth | 14 | Arabe pleine largeur: 1, 2, 3, 4. |
| ArabicHalfWidth | 15 | Arabe demi-largeur: 1, 2, 3, 4. |
| KanjiTraditional | 16 | Japonais légal. |
| KanjiTraditional2 | 17 | Dix mille numériques japonais. |
| NumberInCircle | 18 | Cercles enfermés. |
| DecimalFullWidth | 19 | Largeur pleine décimale: 1, 2, 3, 4. |
| Aiueo | 20 | Aiueo en pleine largeur. |
| Iroha | 21 | Iroha en pleine largeur. |
| LeadingZero | 22 | Zéro initial (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | 23 | Puces (vérifiez le code de caractère dans le texte) |
| Ganada | 24 | Ganada coréen. |
| Chosung | 25 | Corée Chosung. |
| GB1 | 26 | Point final enfermé. |
| GB2 | 27 | Parenthèse enfermée. |
| GB3 | 28 | Cercle enfermé chinois. |
| GB4 | 29 | Idéogramme cercle enfermé. |
| Zodiac1 | 30 | Idéogramme traditionnel. |
| Zodiac2 | 31 | Idéogramme du zodiaque. |
| Zodiac3 | 32 | Idéogramme du zodiaque traditionnel. |
| TradChinNum1 | 33 | Comptage taïwanais. |
| TradChinNum2 | 34 | Idéogramme légal traditionnel. |
| TradChinNum3 | 35 | Comptage taïwanais des milliers. |
| TradChinNum4 | 36 | Numérique taïwanais. |
| SimpChinNum1 | 37 | Comptage chinois. |
| SimpChinNum2 | 38 | Chinois légal simplifié. |
| SimpChinNum3 | 39 | Comptage chinois des milliers. |
| SimpChinNum4 | 40 | Chinois (non implémenté) |
| HanjaRead | 41 | Numérique coréen. |
| HanjaReadDigit | 42 | Comptage coréen. |
| Hangul | 43 | Corée légale. |
| Hanja | 44 | Corée numérique2. |
| Hebrew1 | 45 | Hébreu-1. |
| Arabic1 | 46 | Arabe alpha. |
| Hebrew2 | 47 | Hébreu-2. |
| Arabic2 | 48 | Arabe abjad. |
| HindiLetter1 | 49 | Voyelles hindi. |
| HindiLetter2 | 50 | Consonnes hindi. |
| HindiArabic | 51 | Nombres hindi. |
| HindiCardinalText | 52 | Descriptif hindi (cardinaux) |
| ThaiLetter | 53 | Lettres thaï. |
| ThaiArabic | 54 | Nombres thaï. |
| ThaiCardinalText | 55 | Descriptif thaï (cardinaux) |
| VietCardinalText | 56 | Descriptif vietnamien (cardinaux) |
| NumberInDash | 57 | Format du numéro de page: - 1 -, - 2 -, - 3 -, - 4 -. |
| LowercaseRussian | 58 | Alphabet russe en minuscules. |
| MajusculesRusse | 59 | Alphabet russe en majuscules. |
| None | 255 | Pas de puce ni de numéro. |
| Personnalisé | 65280 | Format de nombre personnalisé. Il n'est pris en charge que par le format DOCX. |


## Exemples



Montre comment appliquer un format de liste personnalisé aux paragraphes lors de l'utilisation de [DocumentBuilder](../documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
// Nous pouvons créer des listes imbriquées en augmentant le niveau de retrait.
// Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un constructeur de document.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Créez une liste à partir d’un modèle Microsoft Word et personnalisez les deux premiers niveaux de cette liste.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// Cette valeur NumberFormat créera des symboles de puces en forme d’étoile.
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// Créez des paragraphes et appliquez les deux niveaux de notre mise en forme de liste personnalisée à ceux‑ci.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
