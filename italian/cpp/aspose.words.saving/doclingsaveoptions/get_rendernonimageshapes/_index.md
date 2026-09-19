---
title: "metodo Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes"
linktitle: "get_RenderNonImageShapes"
second_title: "Riferimento API Aspose.Words per C++"
description: "metodo Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes. Ottiene o imposta un valore che indica se le forme non immagine devono essere renderizzate e scritte nel documento JSON di output Docling in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.saving/doclingsaveoptions/get_rendernonimageshapes/
---
## DoclingSaveOptions::get_RenderNonImageShapes method


Ottiene o imposta un valore che indica se le forme non immagine devono essere renderizzate e scritte nel documento JSON Docling di output.

```cpp
bool Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes() const
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

* Class [DoclingSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
