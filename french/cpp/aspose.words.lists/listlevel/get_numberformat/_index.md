---
title: "Aspose::Words::Lists::ListLevel::get_NumberFormat méthode"
linktitle: "get_NumberFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Lists::ListLevel::get_NumberFormat méthode. Retourne ou définit le format de nombre pour le niveau de liste en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words.lists/listlevel/get_numberformat/
---
## ListLevel::get_NumberFormat method


Renvoie ou définit le format de numéro pour le niveau de liste.

```cpp
System::String Aspose::Words::Lists::ListLevel::get_NumberFormat() const
```

## Remarques


Parmi les caractères de texte normaux, la chaîne peut contenir des caractères de substitution \x0000 à \x0008 représentant les nombres des niveaux de liste correspondants.

Par exemple, la chaîne "\x0000.\x0001)" générera une étiquette de liste ressemblant à "1.5)". Le nombre "1" est le numéro actuel du premier niveau de liste, le nombre "5" est le numéro actuel du deuxième niveau de liste.

Null n'est pas autorisé, mais une chaîne vide signifiant aucun numéro est valide.

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


Présente des façons avancées de personnaliser les libellés de liste.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
// Nous pouvons créer des listes imbriquées en augmentant le niveau de retrait.
// Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un constructeur de document.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

// Les libellés du niveau 1 seront formatés selon le style de paragraphe "Heading 1" et auront un préfixe.
// Ils ressembleront à "Appendix A", "Appendix B"...
list->get_ListLevels()->idx_get(0)->set_NumberFormat(u"Appendix \x0000");
list->get_ListLevels()->idx_get(0)->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseLetter);
list->get_ListLevels()->idx_get(0)->set_LinkedStyle(doc->get_Styles()->idx_get(u"Heading 1"));

// Les libellés du niveau 2 afficheront les numéros actuels du premier et du deuxième niveaux de liste et auront des zéros initiaux.
// Si le premier niveau de liste est à 1, alors les libellés de ces listes ressembleront à "Section (1.01)", "Section (1.02)"...
list->get_ListLevels()->idx_get(1)->set_NumberFormat(u"Section (\x0000" u".\x0001" u")");
list->get_ListLevels()->idx_get(1)->set_NumberStyle(Aspose::Words::NumberStyle::LeadingZero);

// Notez que le niveau supérieur utilise la numérotation UppercaseLetter.
// Nous pouvons définir la propriété "IsLegal" pour utiliser des chiffres arabes pour les niveaux de liste supérieurs.
list->get_ListLevels()->idx_get(1)->set_IsLegal(true);
list->get_ListLevels()->idx_get(1)->set_RestartAfterLevel(0);

// Les libellés du niveau 3 seront des chiffres romains majuscules avec un préfixe et un suffixe et redémarreront à chaque élément du niveau 1 de la liste.
// Ces libellés de liste ressembleront à "-I-", "-II-"...
list->get_ListLevels()->idx_get(2)->set_NumberFormat(u"-\x0002" u"-");
list->get_ListLevels()->idx_get(2)->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
list->get_ListLevels()->idx_get(2)->set_RestartAfterLevel(1);

// Rendez les libellés de tous les niveaux de liste en gras.
for (auto&& level : list->get_ListLevels())
{
    level->get_Font()->set_Bold(true);
}

// Appliquez le formatage de liste au paragraphe actuel.
builder->get_ListFormat()->set_List(list);

// Créez des éléments de liste qui afficheront les trois niveaux de notre liste.
for (int32_t n = 0; n < 2; n++)
{
    for (int32_t i = 0; i < 3; i++)
    {
        builder->get_ListFormat()->set_ListLevelNumber(i);
        builder->Writeln(System::String(u"Level ") + i);
    }
}

builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.CreateListRestartAfterHigher.docx");
```

## Voir aussi

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
