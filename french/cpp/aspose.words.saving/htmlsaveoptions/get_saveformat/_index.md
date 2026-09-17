---
title: "Méthode Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat"
linktitle: "get_SaveFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat. Indique le format dans lequel le document sera enregistré si cet objet d'options de sauvegarde est utilisé. Peut être Html, Mhtml, Epub, Azw3 ou Mobi en C++."
type: docs
weight: 45000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_saveformat/
---
## HtmlSaveOptions::get_SaveFormat method


Indique le format dans lequel le document sera enregistré si cet objet d'options de sauvegarde est utilisé. Peut être [Html](../../../aspose.words/saveformat/), [Mhtml](../../../aspose.words/saveformat/), [Epub](../../../aspose.words/saveformat/), [Azw3](../../../aspose.words/saveformat/) ou [Mobi](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat() override
```


## Exemples



Montre comment utiliser un encodage spécifique lors de l'enregistrement d'un document au format .epub.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Utilisez un objet SaveOptions pour spécifier le codage d'un document que nous allons enregistrer.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// Par défaut, un document .epub de sortie contiendra tous ses éléments dans une seule partie HTML.
// Un critère de division nous permet de segmenter le document en plusieurs parties HTML.
// Nous définirons les critères pour diviser le document en paragraphes d'en-tête.
// Ceci est utile pour les lecteurs qui ne peuvent pas lire des fichiers HTML de taille supérieure à une taille spécifique.
saveOptions->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);

// Spécifiez que nous voulons exporter les propriétés du document.
saveOptions->set_ExportDocumentProperties(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
