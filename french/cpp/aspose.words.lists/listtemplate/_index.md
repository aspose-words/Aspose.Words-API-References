---
title: "Énumération Aspose::Words::Lists::ListTemplate"
linktitle: "ListTemplate"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Énumération Aspose::Words::Lists::ListTemplate. Spécifie l'un des formats de liste prédéfinis disponibles dans Microsoft Word en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.lists/listtemplate/
---
## ListTemplate enum


Spécifie l’un des formats de liste prédéfinis disponibles dans Microsoft Word.

```cpp
enum class ListTemplate
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| BulletDefault | 0 | Liste à puces par défaut avec 9 niveaux. La puce du premier niveau est un disque, celle du deuxième niveau est un cercle, celle du troisième niveau est un carré. Ensuite, le formatage se répète pour les niveaux restants. Chaque niveau est indenté vers la droite de 0.25" par rapport au niveau précédent. Correspond au premier modèle de liste à puces dans la boîte de dialogue Puces et numérotation de Microsoft Word. |
| BulletDisk | n/a | Identique à [BulletDefault](./). Correspond au premier modèle de liste à puces dans la boîte de dialogue Puces et numérotation de Microsoft Word. |
| BulletCircle | n/a | La puce du premier niveau est un cercle. Les niveaux restants sont identiques à ceux de [BulletDefault](./). Correspond au deuxième modèle de liste à puces dans la boîte de dialogue Puces et numérotation de Microsoft Word. |
| BulletSquare | n/a | La puce du premier niveau est un carré. Les niveaux restants sont identiques à ceux de [BulletDefault](./). Correspond au troisième modèle de liste à puces dans la boîte de dialogue Puces et numérotation de Microsoft Word. |
| BulletDiamonds | n/a | La puce du premier niveau est un caractère Wingding 4-diamants. Les niveaux restants sont identiques à ceux de [BulletDefault](./). Correspond au cinquième modèle de liste à puces dans la boîte de dialogue Puces et numérotation de Microsoft Word. |
| BulletArrowHead | n/a | La puce du premier niveau est un caractère Wingding en forme de tête de flèche. Les niveaux restants sont identiques à ceux de [BulletDefault](./). Correspond au sixième modèle de liste à puces dans la boîte de dialogue Puces et numérotation de Microsoft Word. |
| BulletTick | n/a | La puce du premier niveau est un caractère Wingding coche. Les niveaux restants sont identiques à ceux de [BulletDefault](./). Correspond au septième modèle de liste à puces dans la boîte de dialogue Puces et numérotation de Microsoft Word. |
| NumberDefault | n/a | Liste numérotée par défaut avec 9 niveaux. Numérotation arabe (1., 2., 3., ...) pour le premier niveau, numérotation en lettres minuscules (a., b., c., ...) pour le deuxième niveau, numérotation romaine en minuscules (i., ii., iii., ...) pour le troisième niveau. Ensuite, le formatage se répète pour les niveaux restants. Chaque niveau est indenté vers la droite de 0.25" par rapport au niveau précédent. Correspond au premier modèle de liste numérotée dans la boîte de dialogue Puces et numérotation de Microsoft Word. |
| NumberArabicDot | n/a | Identique à [NumberDefault](./). Correspond au premier modèle de liste numérotée dans la boîte de dialogue Puces et numérotation de Microsoft Word. |
| NumberArabicParenthesis | n/a | Le numéro du premier niveau est "1)". Les niveaux restants sont identiques à ceux de [NumberDefault](./). Correspond au deuxième modèle de liste numérotée dans la boîte de dialogue Puces et numérotation de Microsoft Word. |
| NumberUppercaseRomanDot | n/a | Le numéro du premier niveau est "I.". Les niveaux restants sont identiques à ceux de [NumberDefault](./). Correspond au troisième modèle de liste numérotée dans la boîte de dialogue Puces et numérotation de Microsoft Word. |
| NumberUppercaseLetterDot | n/a | Le numéro du premier niveau est "A.". Les niveaux restants sont identiques à ceux de [NumberDefault](./). Correspond au quatrième modèle de liste numérotée dans la boîte de dialogue Puces et numérotation de Microsoft Word. |
| NumberLowercaseLetterParenthesis | n/a | Le numéro du premier niveau est "a)". Les niveaux restants sont identiques à ceux de [NumberDefault](./). Correspond au cinquième modèle de liste numérotée dans la boîte de dialogue Puces et numérotation de Microsoft Word. |
| NumberLowercaseLetterDot | n/a | Le numéro du premier niveau est "a.". Les niveaux restants sont identiques à ceux de [NumberDefault](./). Correspond au sixième modèle de liste numérotée dans la boîte de dialogue Puces et numérotation de Microsoft Word. |
| NumberLowercaseRomanDot | n/a | Le numéro du premier niveau est "i.". Les niveaux restants sont les mêmes que dans [NumberDefault](./). Correspond au 7e modèle de liste numérotée dans la boîte de dialogue Puces et numérotation de Microsoft Word. |
| OutlineNumbers | n/a | Une liste structurée avec des niveaux numérotés "1), a), i), (1), (a), (i), 1., a., i.". Correspond au 1er modèle de liste structurée dans la boîte de dialogue Puces et numérotation de Microsoft Word. |
| OutlineLegal | n/a | Une liste structurée dont les niveaux sont numérotés "1., 1.1., 1.1.1, ...". Correspond au 2e modèle de liste structurée dans la boîte de dialogue Puces et numérotation de Microsoft Word. |
| OutlineBullets | n/a | Des listes structurées avec différents puces pour chaque niveau. Correspond au 3e modèle de liste structurée dans la boîte de dialogue Puces et numérotation de Microsoft Word. |
| OutlineHeadingsArticleSection | n/a | Une liste structurée dont les niveaux sont liés aux styles de titres. Correspond au 4e modèle de liste structurée dans la boîte de dialogue Puces et numérotation de Microsoft Word. |
| OutlineHeadingsLegal | n/a | Une liste structurée dont les niveaux sont liés aux styles de titres. Correspond au 5e modèle de liste structurée dans la boîte de dialogue Puces et numérotation de Microsoft Word. |
| OutlineHeadingsNumbers | n/a | Une liste structurée dont les niveaux sont liés aux styles de titres. Correspond au 6e modèle de liste structurée dans la boîte de dialogue Puces et numérotation de Microsoft Word. |
| OutlineHeadingsChapter | n/a | Une liste structurée dont les niveaux sont liés aux styles de titres. Correspond au 7e modèle de liste structurée dans la boîte de dialogue Puces et numérotation de Microsoft Word. |

## Remarques


Une valeur de modèle de liste est utilisée comme paramètre dans la méthode [Add()](../listcollection/add/).

Les modèles de listes Aspose.Words correspondent aux 21 modèles de listes disponibles dans la boîte de dialogue Puces et numérotation de Microsoft Word 2003.

## Exemples



Montre comment travailler avec les niveaux de listes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
// Nous pouvons créer des listes imbriquées en augmentant le niveau de retrait.
// Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un constructeur de document.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Voici deux types de listes que nous pouvons créer à l'aide d'un constructeur de document.
// 1 -  Une liste numérotée :
// Les listes numérotées créent un ordre logique pour leurs paragraphes en numérotant chaque élément.
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault));

ASSERT_TRUE(builder->get_ListFormat()->get_IsListItem());

// En définissant la propriété "ListLevelNumber", nous pouvons augmenter le niveau de la liste
// pour commencer une sous‑liste autonome à l'élément de liste actuel.
// Le modèle de liste Microsoft Word appelé "NumberDefault" utilise des chiffres pour créer des niveaux de liste pour le premier niveau de liste.
// Les niveaux de liste plus profonds utilisent des lettres et des chiffres romains minuscules.
for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// 2 -  Une liste à puces :
// Cette liste appliquera une indentation et un symbole de puce ("•") avant chaque paragraphe.
// Les niveaux plus profonds de cette liste utiliseront des symboles différents, tels que "■" et "○".
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));

for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// Nous pouvons désactiver le formatage de liste pour ne pas formater les paragraphes suivants comme des listes en désactivant le drapeau "List".
builder->get_ListFormat()->set_List(nullptr);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

doc->Save(get_ArtifactsDir() + u"Lists.SpecifyListLevel.docx");
```


Montre comment redémarrer la numérotation dans une liste en copiant une liste.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
// Nous pouvons créer des listes imbriquées en augmentant le niveau de retrait.
// Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un constructeur de document.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Créez une liste à partir d'un modèle Microsoft Word et personnalisez son premier niveau de liste.
System::SharedPtr<Aspose::Words::Lists::List> list1 = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberArabicParenthesis);
list1->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Red());
list1->get_ListLevels()->idx_get(0)->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);

// Appliquez notre liste à certains paragraphes.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"List 1 starts below:");
builder->get_ListFormat()->set_List(list1);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// Nous pouvons ajouter une copie d'une liste existante à la collection de listes du document
// pour créer une liste similaire sans modifier l'original.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->AddCopy(list1);
list2->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Blue());
list2->get_ListLevels()->idx_get(0)->set_StartAt(10);

// Appliquez la deuxième liste aux nouveaux paragraphes.
builder->Writeln(u"List 2 starts below:");
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.RestartNumberingUsingListCopy.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
