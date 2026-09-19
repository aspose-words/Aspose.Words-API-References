---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat metodo"
linktitle: "get_SaveFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat metodo. Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere Html, Mhtml, Epub, Azw3 o Mobi in C++."
type: docs
weight: 45000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_saveformat/
---
## HtmlSaveOptions::get_SaveFormat method


Specifica il formato in cui il documento verrà salvato se questo oggetto di opzioni di salvataggio è utilizzato. Può essere [Html](../../../aspose.words/saveformat/), [Mhtml](../../../aspose.words/saveformat/), [Epub](../../../aspose.words/saveformat/), [Azw3](../../../aspose.words/saveformat/) o [Mobi](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat() override
```


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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
