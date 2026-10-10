---
title: "Aspose::Words::Saving::PsSaveOptions::get_UseBookFoldPrintingSettings méthode"
linktitle: "get_UseBookFoldPrintingSettings"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::PsSaveOptions::get_UseBookFoldPrintingSettings méthode. Obtient ou définit une valeur booléenne indiquant si le document doit être enregistré en utilisant une mise en page d'impression de livret, si elle est spécifiée via MultiplePages en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.saving/pssaveoptions/get_usebookfoldprintingsettings/
---
## PsSaveOptions::get_UseBookFoldPrintingSettings method


Obtient ou définit une valeur booléenne indiquant si le document doit être enregistré en utilisant une mise en page d'impression en livret, si elle est spécifiée via [MultiplePages](../../../aspose.words/pagesetup/get_multiplepages/).

```cpp
bool Aspose::Words::Saving::PsSaveOptions::get_UseBookFoldPrintingSettings() const
```

## Remarques


Si cette option est spécifiée, [PageSet](../../fixedpagesaveoptions/get_pageset/) est ignoré lors de l'enregistrement. Ce comportement correspond à MS Word. Si les paramètres d'impression en livret ne sont pas spécifiés dans la configuration de la page, cette option n'aura aucun effet.

## Exemples



Montre comment enregistrer un document au format Postscript sous forme de pliage de livre.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

// Créez un objet "PsSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en PostScript.
// Définissez la propriété "UseBookFoldPrintingSettings" sur "true" pour organiser le contenu
// dans le document Postscript de sortie de manière à nous permettre d'en faire un livret.
// Définissez la propriété "UseBookFoldPrintingSettings" sur "false" pour enregistrer le document normalement.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::PsSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Ps);
saveOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// Si nous rendons le document sous forme de livret, nous devons définir la propriété "MultiplePages"
// propriétés des objets de configuration de page de toutes les sections à \"MultiplePagesType.BookFoldPrinting\".
for (auto&& s : System::IterateOver<Aspose::Words::Section>(doc->get_Sections()))
{
    s->get_PageSetup()->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);
}

// Une fois que nous imprimons ce document des deux côtés des pages, nous pouvons plier toutes les pages au milieu en une seule fois,
// et le contenu s'alignera de manière à créer un livret.
doc->Save(get_ArtifactsDir() + u"PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

## Voir aussi

* Class [PsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
