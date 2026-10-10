---
title: "Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode method"
linktitle: "get_FontEmbeddingMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode method. Specifica la modalità di incorporamento dei font in C++."
type: docs
weight: 18000
url: /it/cpp/aspose.words.saving/pdfsaveoptions/get_fontembeddingmode/
---
## PdfSaveOptions::get_FontEmbeddingMode method


Specifica la modalità di incorporamento dei caratteri.

```cpp
Aspose::Words::Saving::PdfFontEmbeddingMode Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode() const
```

## Note


Il valore predefinito è [EmbedAll](../../pdffontembeddingmode/).

Questa impostazione funziona solo per il testo con codifica ANSI (Windows-1252). Se il documento contiene testo non ANSI, i caratteri corrispondenti verranno incorporati indipendentemente da questa impostazione.

La conformità a PDF/A e PDF/UA richiede che tutti i caratteri siano incorporati. Il valore [EmbedAll](../../pdffontembeddingmode/) verrà usato automaticamente durante il salvataggio in PDF/A e PDF/UA.
## Vedi anche

* Enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
