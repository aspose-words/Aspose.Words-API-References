---
title: "Aspose::Words::Saving::PsSaveOptions::get_SaveFormat méthode"
linktitle: "get_SaveFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::PsSaveOptions::get_SaveFormat méthode. Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Ne peut être que Ps en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.saving/pssaveoptions/get_saveformat/
---
## PsSaveOptions::get_SaveFormat method


Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Ne peut être que [Ps](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::PsSaveOptions::get_SaveFormat() override
```


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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [PsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
