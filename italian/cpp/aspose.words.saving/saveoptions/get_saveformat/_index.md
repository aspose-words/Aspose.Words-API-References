---
title: "Metodo Aspose::Words::Saving::SaveOptions::get_SaveFormat"
linktitle: "get_SaveFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::SaveOptions::get_SaveFormat. Specifica il formato in cui il documento verrà salvato se questo oggetto SaveOptions viene utilizzato in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words.saving/saveoptions/get_saveformat/
---
## SaveOptions::get_SaveFormat method


Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio.

```cpp
virtual Aspose::Words::SaveFormat Aspose::Words::Saving::SaveOptions::get_SaveFormat()=0
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
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
