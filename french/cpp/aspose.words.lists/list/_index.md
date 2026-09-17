---
title: "Aspose::Words::Lists::List class"
linktitle: "List"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Lists::List class. Représente la mise en forme d’une liste. Pour en savoir plus, consultez l’article de documentation en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.lists/list/
---
## List class


Représente le formatage d’une liste. Pour en savoir plus, consultez l’article de documentation [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class List : public System::IComparable<System::SharedPtr<Aspose::Words::Lists::List>>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [CompareTo](./compareto/)(System::SharedPtr\<Aspose::Words::Lists::List\>) override | Compare la liste spécifiée à la liste actuelle. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Compare avec la liste spécifiée. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |
| [get_Document](./get_document/)() const | Obtient le document propriétaire. |
| [get_IsListStyleDefinition](./get_isliststyledefinition/)() | Renvoie **true** si cette liste est une définition d’un style de liste. |
| [get_IsListStyleReference](./get_isliststylereference/)() | Renvoie **true** si cette liste est une référence à un style de liste. |
| [get_IsMultiLevel](./get_ismultilevel/)() | Renvoie **true** lorsque la liste contient 9 niveaux ; **false** lorsqu’elle ne contient qu’un niveau. |
| [get_IsRestartAtEachSection](./get_isrestartateachsection/)() | Spécifie si la liste doit être redémarrée à chaque section. La valeur par défaut est **false**. |
| [get_ListId](./get_listid/)() const | Obtient l’identifiant unique de la liste. |
| [get_ListLevels](./get_listlevels/)() | Obtient la collection des niveaux de liste pour cette liste. |
| [get_Style](./get_style/)() | Obtient le style de liste que cette liste référence ou définit. |
| [GetHashCode](./gethashcode/)() const override | Calcule le code de hachage pour cet objet liste. |
| [GetType](./gettype/)() const override |  |
| [HasSameTemplate](./hassametemplate/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Renvoie true si la liste actuelle et la liste donnée sont créées à partir du même modèle. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsRestartAtEachSection](./set_isrestartateachsection/)(bool) | Mutateur pour [Aspose::Words::Lists::List::get_IsRestartAtEachSection](./get_isrestartateachsection/). |
| static [Type](./type/)() |  |
## Remarques


Une liste dans un document Microsoft Word est un ensemble de propriétés de mise en forme de liste. Chaque liste peut comporter jusqu’à 9 niveaux et des propriétés de mise en forme, telles que le style de numérotation, la valeur de départ, le retrait, la position de tabulation, etc., sont définies séparément pour chaque niveau.

Un objet [List](./) appartient toujours à la collection [ListCollection](../listcollection/).

Pour créer une nouvelle liste, utilisez les méthodes Add de la collection [ListCollection](../listcollection/).

Pour modifier la mise en forme d’une liste, utilisez les objets [ListLevel](../listlevel/) présents dans la collection [ListLevels](./get_listlevels/).

Pour appliquer ou supprimer la mise en forme de liste d’un paragraphe, utilisez [ListFormat](../listformat/).

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


Montre comment appliquer une mise en forme de liste personnalisée aux paragraphes lors de l’utilisation de [DocumentBuilder](../../aspose.words/documentbuilder/).
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
