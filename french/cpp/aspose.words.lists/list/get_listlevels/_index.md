---
title: "Aspose::Words::Lists::List::get_ListLevels méthode"
linktitle: "get_ListLevels"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Lists::List::get_ListLevels méthode. Obtient la collection des niveaux de liste pour cette liste en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.lists/list/get_listlevels/
---
## List::get_ListLevels method


Obtient la collection des niveaux de liste pour cette liste.

```cpp
System::SharedPtr<Aspose::Words::Lists::ListLevelCollection> Aspose::Words::Lists::List::get_ListLevels()
```

## Remarques


Utilisez cette propriété pour accéder et modifier le formatage propre à chaque niveau de la liste.

## Exemples



Montre comment appliquer un formatage de liste personnalisé aux paragraphes lors de l’utilisation de [DocumentBuilder](../../../aspose.words/documentbuilder/).
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

* Class [ListLevelCollection](../../listlevelcollection/)
* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
