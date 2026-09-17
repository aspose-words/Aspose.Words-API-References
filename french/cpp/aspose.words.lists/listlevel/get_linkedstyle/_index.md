---
title: "Méthode Aspose::Words::Lists::ListLevel::get_LinkedStyle"
linktitle: "get_LinkedStyle"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Lists::ListLevel::get_LinkedStyle. Obtient ou définit le style de paragraphe lié à ce niveau de liste en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.lists/listlevel/get_linkedstyle/
---
## ListLevel::get_LinkedStyle method


Obtient ou définit le style de paragraphe lié à ce niveau de liste.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::Lists::ListLevel::get_LinkedStyle()
```

## Remarques


Cette propriété est **null** lorsque le niveau de liste n’est pas lié à un style de paragraphe. Cette propriété peut être définie sur **null**.

## Exemples



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

* Class [Style](../../../aspose.words/style/)
* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
