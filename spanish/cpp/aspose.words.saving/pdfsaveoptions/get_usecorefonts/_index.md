---
title: "Método Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts"
linktitle: "get_UseCoreFonts"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts. Obtiene o establece un valor que determina si se sustituyen o no las fuentes TrueType Arial, Times New Roman, Courier New y Symbol por fuentes PDF Type 1 básicas en C++."
type: docs
weight: 32000
url: /es/cpp/aspose.words.saving/pdfsaveoptions/get_usecorefonts/
---
## PdfSaveOptions::get_UseCoreFonts method


Obtiene o establece un valor que determina si se deben sustituir las fuentes TrueType Arial, Times New Roman, Courier New y Symbol por fuentes PDF Type 1 básicas.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts() const
```

## Observaciones


El valor predeterminado es **false**. Cuando este valor se establece en **true**, las fuentes Arial, Times New Roman, Courier New y Symbol se reemplazan en el documento PDF por la fuente Type 1 básica correspondiente.

Las fuentes PDF básicas, o sus métricas de fuente y fuentes de sustitución adecuadas, deben estar disponibles para cualquier aplicación visor de PDF.

Esta configuración funciona solo para el texto en codificación ANSI (Windows‑1252). El texto no ANSI se escribirá con una fuente TrueType incrustada sin importar esta configuración.

El cumplimiento de PDF/A y PDF/UA requiere que todas las fuentes estén incrustadas. El valor **false** se usará automáticamente al guardar en PDF/A y PDF/UA.

Las fuentes básicas no son compatibles al guardar en formato PDF 2.0. El valor **false** se usará automáticamente al guardar en PDF 2.0.

Esta opción tiene una prioridad mayor que la opción [FontEmbeddingMode](../get_fontembeddingmode/).
## Ver también

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
