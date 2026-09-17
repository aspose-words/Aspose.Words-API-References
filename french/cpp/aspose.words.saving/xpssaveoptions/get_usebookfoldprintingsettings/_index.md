---
title: "Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings méthode"
linktitle: "get_UseBookFoldPrintingSettings"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings méthode. Obtient ou définit une valeur booléenne indiquant si le document doit être enregistré en utilisant une mise en page d'impression en livret, si elle est spécifiée via MultiplePages en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.saving/xpssaveoptions/get_usebookfoldprintingsettings/
---
## XpsSaveOptions::get_UseBookFoldPrintingSettings method


Obtient ou définit une valeur booléenne indiquant si le document doit être enregistré en utilisant une mise en page d'impression en livret, si elle est spécifiée via [MultiplePages](../../../aspose.words/pagesetup/get_multiplepages/).

```cpp
bool Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings() const
```

## Remarques


Si cette option est spécifiée, [PageSet](../../fixedpagesaveoptions/get_pageset/) est ignoré lors de l'enregistrement. Ce comportement correspond à MS Word. Si les paramètres d'impression en livret ne sont pas spécifiés dans la configuration de la page, cette option n'aura aucun effet.

## Exemples



Montre comment enregistrer un document au format XPS sous forme de pliage de livre.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

// Créez un objet "XpsSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .XPS.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>(Aspose::Words::SaveFormat::Xps);

// Définissez la propriété "UseBookFoldPrintingSettings" sur "true" pour organiser le contenu
// dans le XPS de sortie d'une manière qui nous aide à l'utiliser pour créer un livret.
// Définissez la propriété "UseBookFoldPrintingSettings" sur "false" pour rendre le XPS normalement.
xpsOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// Si nous rendons le document sous forme de livret, nous devons définir la propriété "MultiplePages"
// propriétés des objets de configuration de page de toutes les sections à \"MultiplePagesType.BookFoldPrinting\".
if (renderTextAsBookFold)
{
    for (auto&& s : System::IterateOver<Aspose::Words::Section>(doc->get_Sections()))
    {
        s->get_PageSetup()->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);
    }
}

// Une fois que nous imprimons ce document, nous pouvons le transformer en livret en empilant les pages
// pour sortir de l'imprimante et se plier au milieu.
doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.BookFold.xps", xpsOptions);
```

## Voir aussi

* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
