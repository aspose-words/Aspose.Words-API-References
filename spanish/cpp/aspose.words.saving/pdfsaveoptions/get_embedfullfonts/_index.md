---
title: "Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts método"
linktitle: "get_EmbedFullFonts"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts método. Controla cómo se incrustan las fuentes en los documentos PDF resultantes en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words.saving/pdfsaveoptions/get_embedfullfonts/
---
## PdfSaveOptions::get_EmbedFullFonts method


Controla cómo se incrustan las fuentes en los documentos PDF resultantes.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts() const
```

## Observaciones


El valor predeterminado es **false**, lo que significa que las fuentes se reducen a subconjuntos antes de incrustarlas. El subconjunto es útil si deseas mantener el tamaño del archivo de salida más pequeño. El subconjunto elimina todos los glifos no utilizados de una fuente.

Cuando este valor se establece en **true**, se incruta un archivo de fuente completo en el PDF sin subconjunto. Esto producirá archivos de salida más grandes, pero puede ser una opción útil cuando deseas editar el PDF resultante más tarde (p. ej., agregar más texto).

Algunas fuentes son grandes (varios megabytes) y su incrustación sin subconjunto producirá documentos de salida de gran tamaño.
## Ver también

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
