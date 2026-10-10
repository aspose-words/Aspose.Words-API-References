---
title: "Aspose::Words::Saving::DocumentSplitCriteria enum"
linktitle: "DocumentSplitCriteria"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::DocumentSplitCriteria enum. Spécifie comment le document est découpé en parties lors de l'enregistrement au format Html, Epub ou Azw3 en C++."
type: docs
weight: 52000
url: /fr/cpp/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enum


Spécifie comment le document est découpé en parties lors de l'enregistrement au format [Html](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/) ou [Azw3](../../aspose.words/saveformat/).

```cpp
enum class DocumentSplitCriteria
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 | Le document n'est pas découpé. |
| PageBreak | 1 | Le document est découpé en parties aux sauts de page explicites. Un saut de page peut être spécifié par un caractère [PageBreak](../../aspose.words/controlchar/pagebreak/), un saut de section indiquant le début d'une nouvelle section sur une nouvelle page, ou un paragraphe dont la propriété [PageBreakBefore](../../aspose.words/paragraphformat/get_pagebreakbefore/) est définie sur **true**. |
| ColumnBreak | 2 | Le document est découpé en parties aux sauts de colonne. Un saut de colonne peut être spécifié par un caractère [ColumnBreak](../../aspose.words/controlchar/columnbreak/) ou un saut de section indiquant le début d'une nouvelle section dans une nouvelle colonne. |
| SectionBreak | 4 | Le document est découpé en parties à un saut de section de tout type. |
| HeadingParagraph | 8 | Le document est découpé en parties à un paragraphe formaté avec un style de titre **Heading 1**, **Heading 2** etc. Utilisez-le conjointement avec [DocumentSplitHeadingLevel](../htmlsaveoptions/get_documentsplitheadinglevel/) pour spécifier les niveaux de titre (de 1 au niveau indiqué) où découper. |

## Remarques


[DocumentSplitCriteria](./) is a set of flags which can be combined. For instance you can split the document at page breaks and heading paragraphs in the same export operation.

Différents critères peuvent se chevaucher partiellement. Par exemple, le style **Heading 1** reçoit fréquemment la propriété [PageBreakBefore](../../aspose.words/paragraphformat/get_pagebreakbefore/), ce qui le place sous deux critères : [PageBreak](./) et [HeadingParagraph](./). Certains sauts de section peuvent provoquer des sauts de page, etc. Dans la plupart des cas, spécifier un seul indicateur est l'option la plus pratique.

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
