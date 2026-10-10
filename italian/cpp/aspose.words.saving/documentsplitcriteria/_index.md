---
title: "Aspose::Words::Saving::DocumentSplitCriteria enum"
linktitle: "DocumentSplitCriteria"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::DocumentSplitCriteria enum. Specifica come il documento viene suddiviso in parti durante il salvataggio nei formati Html, Epub o Azw3 in C++."
type: docs
weight: 52000
url: /it/cpp/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enum


Specificare come il documento viene suddiviso in parti durante il salvataggio nei formati [Html](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/) o [Azw3](../../aspose.words/saveformat/).

```cpp
enum class DocumentSplitCriteria
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | Il documento non viene suddiviso. |
| PageBreak | 1 | Il documento è suddiviso in parti in corrispondenza di interruzioni di pagina esplicite. Un'interruzione di pagina può essere specificata mediante un carattere [PageBreak](../../aspose.words/controlchar/pagebreak/), un'interruzione di sezione che indica l'inizio di una nuova sezione su una nuova pagina, o un paragrafo il cui proprietà [PageBreakBefore](../../aspose.words/paragraphformat/get_pagebreakbefore/) è impostata su **true**. |
| ColumnBreak | 2 | Il documento è suddiviso in parti in corrispondenza di interruzioni di colonna. Un'interruzione di colonna può essere specificata mediante un carattere [ColumnBreak](../../aspose.words/controlchar/columnbreak/) o un'interruzione di sezione che indica l'inizio di una nuova sezione in una nuova colonna. |
| SectionBreak | 4 | Il documento è suddiviso in parti in corrispondenza di un'interruzione di sezione di qualsiasi tipo. |
| HeadingParagraph | 8 | Il documento è suddiviso in parti in corrispondenza di un paragrafo formattato con uno stile di intestazione **Heading 1**, **Heading 2** ecc. Utilizzare insieme a [DocumentSplitHeadingLevel](../htmlsaveoptions/get_documentsplitheadinglevel/) per specificare i livelli di intestazione (da 1 al livello specificato) in cui effettuare la suddivisione. |

## Note


[DocumentSplitCriteria](./) is a set of flags which can be combined. For instance you can split the document at page breaks and heading paragraphs in the same export operation.

Diversi criteri possono sovrapporsi parzialmente. Ad esempio, lo stile **Heading 1** è spesso associato alla proprietà [PageBreakBefore](../../aspose.words/paragraphformat/get_pagebreakbefore/), quindi rientra in due criteri: [PageBreak](./) e [HeadingParagraph](./). Alcune interruzioni di sezione possono causare interruzioni di pagina e così via. Nei casi tipici, specificare un solo flag è l'opzione più pratica.

## Esempi



Mostra come utilizzare una codifica specifica durante il salvataggio di un documento in .epub.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Utilizza un oggetto SaveOptions per specificare la codifica di un documento che salveremo.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// Per impostazione predefinita, un documento di output .epub avrà tutti i suoi contenuti in un'unica parte HTML.
// Un criterio di divisione ci consente di segmentare il documento in diverse parti HTML.
// Imposteremo i criteri per dividere il documento in paragrafi di intestazione.
// Questo è utile per i lettori che non possono leggere file HTML più grandi di una dimensione specifica.
saveOptions->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);

// Specifica che desideriamo esportare le proprietà del documento.
saveOptions->set_ExportDocumentProperties(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
