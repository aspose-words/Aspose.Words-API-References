---
title: "Aspose::Words::StyleCollection::Add méthode"
linktitle: "Add"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::StyleCollection::Add méthode. Crée un nouveau style défini par l'utilisateur et l'ajoute à la collection en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/stylecollection/add/
---
## StyleCollection::Add method


Crée un nouveau style défini par l'utilisateur et l'ajoute à la collection.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::Add(Aspose::Words::StyleType type, const System::String &name)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| type | Aspose::Words::StyleType | Une valeur [StyleType](../../styletype/) qui spécifie le type de style à créer. |
| name | const System::String\& | Nom sensible à la casse du style à créer. |
## Remarques


Vous pouvez créer un style de caractère, de paragraphe ou de liste.

Lors de la création d'un style de liste, le style est créé avec le format de liste numérotée par défaut (1 \\ a \\ i).

Lance une exception si un style portant ce nom existe déjà.

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


Montre comment ajouter un [Style](../../style/) à la collection de styles d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Définissez les paramètres par défaut pour les nouveaux styles que nous pourrons ajouter ultérieurement à cette collection.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Si nous ajoutons un style de "StyleType.Paragraph", la collection appliquera les valeurs de
// sa propriété "DefaultParagraphFormat" à la propriété "ParagraphFormat" du style.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Ajoutez un style, puis vérifiez qu’il possède les paramètres par défaut.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Voir aussi

* Class [Style](../../style/)
* Enum [StyleType](../../styletype/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
