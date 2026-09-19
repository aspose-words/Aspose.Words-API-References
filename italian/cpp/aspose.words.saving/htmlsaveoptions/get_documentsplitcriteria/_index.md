---
title: "Metodo Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria"
linktitle: "get_DocumentSplitCriteria"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria. Specifica come il documento deve essere suddiviso durante il salvataggio nei formati Html, Epub o Azw3. Il valore predefinito è None per HTML e HeadingParagraph per EPUB e AZW3 in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_documentsplitcriteria/
---
## HtmlSaveOptions::get_DocumentSplitCriteria method


Specifica come il documento deve essere suddiviso durante il salvataggio nei formati [Html](../../../aspose.words/saveformat/), [Epub](../../../aspose.words/saveformat/) o [Azw3](../../../aspose.words/saveformat/). Il valore predefinito è [None](../../documentsplitcriteria/) per HTML e [HeadingParagraph](../../documentsplitcriteria/) per EPUB e AZW3.

```cpp
Aspose::Words::Saving::DocumentSplitCriteria Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria() const
```

## Note


Normalmente vorresti che un documento fosse salvato in HTML come un unico file. Ma in alcuni casi è preferibile dividere l'output in diverse pagine HTML più piccole. Quando si salva in formato HTML queste pagine verranno generate in file o stream individuali. Quando si salva in formato EPUB saranno incorporate nei relativi pacchetti.

Un documento non può essere diviso durante il salvataggio in formato MHTML.

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

* Enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
