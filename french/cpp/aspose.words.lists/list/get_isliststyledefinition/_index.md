---
title: "Aspose::Words::Lists::List::get_IsListStyleDefinition méthode"
linktitle: "get_IsListStyleDefinition"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Lists::List::get_IsListStyleDefinition méthode. Retourne true si cette liste est une définition d'un style de liste en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.lists/list/get_isliststyledefinition/
---
## List::get_IsListStyleDefinition method


Renvoie **true** si cette liste est une définition d’un style de liste.

```cpp
bool Aspose::Words::Lists::List::get_IsListStyleDefinition()
```

## Remarques


Lorsque cette propriété est **true**, la propriété [Style](../get_style/) renvoie le style de liste que cette liste définit.

En modifiant les propriétés d'une liste qui définit un style de liste, vous modifiez les propriétés du style de liste.

Une liste qui est une définition d'un style de liste ne peut pas être appliquée directement aux paragraphes pour les numéroter.

## Exemples



Montre comment créer un style de liste et l'utiliser dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
// Nous pouvons créer des listes imbriquées en augmentant le niveau de retrait.
// Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un constructeur de document.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Nous pouvons contenir un objet List complet au sein d'un style.
System::SharedPtr<Aspose::Words::Style> listStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle");

System::SharedPtr<Aspose::Words::Lists::List> list1 = listStyle->get_List();

ASSERT_TRUE(list1->get_IsListStyleDefinition());
ASSERT_FALSE(list1->get_IsListStyleReference());
ASSERT_TRUE(list1->get_IsMultiLevel());
ASPOSE_ASSERT_EQ(listStyle, list1->get_Style());

// Modifiez l'apparence de tous les niveaux de liste dans notre liste.
for (auto&& level : list1->get_ListLevels())
{
    level->get_Font()->set_Name(u"Verdana");
    level->get_Font()->set_Color(System::Drawing::Color::get_Blue());
    level->get_Font()->set_Bold(true);
}

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Using list style first time:");

// Créez une autre liste à partir d'une liste dans un style.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->Add(listStyle);

ASSERT_FALSE(list2->get_IsListStyleDefinition());
ASSERT_TRUE(list2->get_IsListStyleReference());
ASPOSE_ASSERT_EQ(listStyle, list2->get_Style());

// Ajoutez quelques éléments de liste que notre liste formattera.
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

builder->Writeln(u"Using list style second time:");

// Créez et appliquez une autre liste basée sur le style de liste.
System::SharedPtr<Aspose::Words::Lists::List> list3 = doc->get_Lists()->Add(listStyle);
builder->get_ListFormat()->set_List(list3);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateAndUseListStyle.docx");
```

## Voir aussi

* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
