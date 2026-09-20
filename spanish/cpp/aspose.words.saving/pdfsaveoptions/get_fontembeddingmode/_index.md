---
title: "Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode method"
linktitle: "get_FontEmbeddingMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode method. Especifica el modo de incrustación de fuentes en C++."
type: docs
weight: 18000
url: /es/cpp/aspose.words.saving/pdfsaveoptions/get_fontembeddingmode/
---
## PdfSaveOptions::get_FontEmbeddingMode method


Especifica el modo de incrustación de fuentes.

```cpp
Aspose::Words::Saving::PdfFontEmbeddingMode Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode() const
```

## Observaciones


El valor predeterminado es [EmbedAll](../../pdffontembeddingmode/).

Esta configuración funciona solo para el texto en codificación ANSI (Windows-1252). Si el documento contiene texto no ANSI, entonces las fuentes correspondientes se incrustarán sin importar esta configuración.

El cumplimiento de PDF/A y PDF/UA requiere que todas las fuentes se incrusten. El valor [EmbedAll](../../pdffontembeddingmode/) se utilizará automáticamente al guardar en PDF/A y PDF/UA.
## Ver también

* Enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
