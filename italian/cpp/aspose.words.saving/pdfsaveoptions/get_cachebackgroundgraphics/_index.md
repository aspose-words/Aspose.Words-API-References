---
title: "Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics method"
linktitle: "get_CacheBackgroundGraphics"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics method. Ottiene o imposta un valore che determina se memorizzare nella cache o meno la grafica posizionata nello sfondo del documento in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.saving/pdfsaveoptions/get_cachebackgroundgraphics/
---
## PdfSaveOptions::get_CacheBackgroundGraphics method


Ottiene o imposta un valore che determina se memorizzare nella cache o meno le grafiche posizionate nello sfondo del documento.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics() const
```

## Note


Il valore predefinito è **true** e la grafica di sfondo viene scritta nel documento PDF come un xObject.

Quando il valore è **false** la grafica di sfondo non viene memorizzata nella cache.

Alcune forme non sono supportate per la memorizzazione nella cache (forme con campi, segnalibri, HRefs).

[Document](../../../aspose.words/document/) background graphic is various shapes, charts, images placed in the footer or header, well as background and border of a page. 
## Vedi anche

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
