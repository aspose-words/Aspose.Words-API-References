---
title: "Aspose::Words::Lists::ListFormat::get_ListLevelNumber method"
linktitle: "get_ListLevelNumber"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Lists::ListFormat::get_ListLevelNumber method. Obtient ou définit le numéro de niveau de liste (0 à 8) pour le paragraphe en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.lists/listformat/get_listlevelnumber/
---
## ListFormat::get_ListLevelNumber method


Obtient ou définit le numéro du niveau de liste (0 à 8) pour le paragraphe.

```cpp
int32_t Aspose::Words::Lists::ListFormat::get_ListLevelNumber()
```

## Remarques


Dans les documents Word, les listes peuvent comporter de 1 à 9 niveaux, numérotés de 0 à 8.

N’a d’effet que lorsque la propriété [List](../get_list/) est définie pour référencer une liste valide.

## Exemples



Montre comment créer des listes à puces et numérotées.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Aspose.Words main advantages are:");

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
// Nous pouvons créer des listes imbriquées en augmentant le niveau de retrait.
// Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un constructeur de document.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Ci-dessous se trouvent deux types de listes que nous pouvons créer avec un constructeur de document.
// 1 -  Une liste à puces :
// Cette liste appliquera une indentation et un symbole de puce ("•") avant chaque paragraphe.
builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Great performance");
builder->Writeln(u"High reliability");
builder->Writeln(u"Quality code and working");
builder->Writeln(u"Wide variety of features");
builder->Writeln(u"Easy to understand API");

// Terminez la liste à puces.
builder->get_ListFormat()->RemoveNumbers();

builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
builder->Writeln(u"Aspose.Words allows:");

// 2 -  Une liste numérotée :
// Les listes numérotées créent un ordre logique pour leurs paragraphes en numérotant chaque élément.
builder->get_ListFormat()->ApplyNumberDefault();

// Ce paragraphe est le premier élément. Le premier élément d’une liste numérotée aura un « 1. » comme symbole d’élément de liste.
builder->Writeln(u"Opening documents from different formats:");

ASSERT_EQ(0, builder->get_ListFormat()->get_ListLevelNumber());

// Appelez la méthode "ListIndent" pour augmenter le niveau de liste actuel,
// ce qui démarrera une nouvelle liste autonome, avec un retrait plus important, à l'élément actuel du premier niveau de liste.
builder->get_ListFormat()->ListIndent();

ASSERT_EQ(1, builder->get_ListFormat()->get_ListLevelNumber());

// Voici les trois premiers éléments de liste du deuxième niveau, qui maintiendront une numérotation
// indépendamment de la numérotation du premier niveau de liste. Selon le format de liste actuel,
// ils auront les symboles "a.", "b.", et "c.".
builder->Writeln(u"DOC");
builder->Writeln(u"PDF");
builder->Writeln(u"HTML");

// Appelez la méthode "ListOutdent" pour revenir au niveau de liste précédent.
builder->get_ListFormat()->ListOutdent();

ASSERT_EQ(0, builder->get_ListFormat()->get_ListLevelNumber());

// Ces deux paragraphes continueront la numérotation du premier niveau de liste.
// Ces éléments auront les symboles "2.", et "3."
builder->Writeln(u"Processing documents");
builder->Writeln(u"Saving documents in different formats:");

// Si nous augmentons le niveau de liste à un niveau auquel nous avons déjà ajouté des éléments,
// la liste imbriquée sera distincte de la précédente, et sa numérotation recommencera depuis le début.
// Ces éléments de liste auront les symboles "a.", "b.", "c.", "d.", et "e".
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"DOC");
builder->Writeln(u"PDF");
builder->Writeln(u"HTML");
builder->Writeln(u"MHTML");
builder->Writeln(u"Plain text");

// Réduisez à nouveau le niveau de liste.
builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"Doing many other things!");

// Terminez la liste numérotée.
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.ApplyDefaultBulletsAndNumbers.docx");
```


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

## Voir aussi

* Class [ListFormat](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
