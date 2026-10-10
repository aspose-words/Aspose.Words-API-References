---
title: "metodo Aspose::Words::Saving::DoclingSaveOptions::get_SaveFormat"
linktitle: "get_SaveFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "metodo Aspose::Words::Saving::DoclingSaveOptions::get_SaveFormat. Specifica il formato in cui il documento verrà salvato se questo oggetto di opzioni di salvataggio viene utilizzato. Può essere solo Docling in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.saving/doclingsaveoptions/get_saveformat/
---
## DoclingSaveOptions::get_SaveFormat method


Specifica il formato in cui il documento verrà salvato se questo oggetto di opzioni di salvataggio viene utilizzato. Può essere solo [Docling](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::DoclingSaveOptions::get_SaveFormat() override
```


## Esempi



Mostra come salvare un documento in formato JSON Docling.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::DoclingSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docling);
// Imposta su true per renderizzare le forme non immagine e includerle nell'output.
// Imposta su false (predefinito) per escludere le forme non immagine dall'output.
saveOptions->set_RenderNonImageShapes(true);

doc->Save(get_ArtifactsDir() + u"Document.DoclingJson.json", saveOptions);
```

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [DoclingSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
