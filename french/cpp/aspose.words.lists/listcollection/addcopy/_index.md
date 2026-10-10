---
title: "Aspose::Words::Lists::ListCollection::AddCopy méthode"
linktitle: "AddCopy"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Lists::ListCollection::AddCopy méthode. Crée une nouvelle liste en copiant la liste spécifiée et en l'ajoutant à la collection de listes du document en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.lists/listcollection/addcopy/
---
## ListCollection::AddCopy method


Crée une nouvelle liste en copiant la liste spécifiée et l'ajoute à la collection de listes du document.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::AddCopy(const System::SharedPtr<Aspose::Words::Lists::List> &srcList)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| srcList | const System::SharedPtr\<Aspose::Words::Lists::List\>\& | La liste source à copier. |

### ReturnValue

La liste nouvellement créée.
## Remarques


La liste source peut provenir de n'importe quel document. Si la liste source appartient à un document différent, une copie de la liste est créée et ajoutée au document actuel.

Si la liste source est une référence ou une définition d'un style de liste, la liste nouvellement créée n'est pas liée au style de liste original.

## Exemples



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

* Class [List](../../list/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
