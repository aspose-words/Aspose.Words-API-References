---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag metodo"
linktitle: "get_ExportLanguageToSpanTag"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag metodo. Ottiene o imposta un valore che determina se creare o meno un tag \"Span\" nella struttura del documento per esportare la lingua del testo in C++."
type: docs
weight: 17000
url: /it/cpp/aspose.words.saving/pdfsaveoptions/get_exportlanguagetospantag/
---
## PdfSaveOptions::get_ExportLanguageToSpanTag method


Ottiene o imposta un valore che determina se creare o meno un tag "Span" nella struttura del documento per esportare la lingua del testo.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag() const
```

## Note


Il valore predefinito è **false** e l'attributo "Lang" è collegato a una sequenza di contenuto marcato in un flusso di contenuto della pagina.

Quando il valore è **true** viene creato un tag "Span" per il testo con lingua non predefinita e l'attributo "Lang" è collegato a questo tag.

Questo valore è ignorato quando [ExportDocumentStructure](../get_exportdocumentstructure/) è **false**.
## Vedi anche

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
