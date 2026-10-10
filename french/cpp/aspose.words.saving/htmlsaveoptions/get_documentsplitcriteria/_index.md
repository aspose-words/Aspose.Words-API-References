---
title: "Méthode Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria"
linktitle: "get_DocumentSplitCriteria"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria. Spécifie comment le document doit être découpé lors de l'enregistrement au format Html, Epub ou Azw3. La valeur par défaut est None pour HTML et HeadingParagraph pour EPUB et AZW3 en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_documentsplitcriteria/
---
## HtmlSaveOptions::get_DocumentSplitCriteria method


Spécifie comment le document doit être découpé lors de l'enregistrement au format [Html](../../../aspose.words/saveformat/), [Epub](../../../aspose.words/saveformat/) ou [Azw3](../../../aspose.words/saveformat/). La valeur par défaut est [None](../../documentsplitcriteria/) pour HTML et [HeadingParagraph](../../documentsplitcriteria/) pour EPUB et AZW3.

```cpp
Aspose::Words::Saving::DocumentSplitCriteria Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria() const
```

## Remarques


Normalement, vous voudriez qu'un document soit enregistré au format HTML en un seul fichier. Mais dans certains cas, il est préférable de diviser la sortie en plusieurs pages HTML plus petites. Lors de l'enregistrement au format HTML, ces pages seront générées dans des fichiers ou des flux individuels. Lors de l'enregistrement au format EPUB, elles seront incorporées dans les packages correspondants.

Un document ne peut pas être divisé lors de l'enregistrement au format MHTML.

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

* Enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
