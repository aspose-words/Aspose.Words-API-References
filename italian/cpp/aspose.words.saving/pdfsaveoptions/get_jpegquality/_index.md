---
title: "Metodo Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality"
linktitle: "get_JpegQuality"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality. Ottiene o imposta un valore che determina la qualità delle immagini JPEG all'interno del documento PDF in C++."
type: docs
weight: 23000
url: /it/cpp/aspose.words.saving/pdfsaveoptions/get_jpegquality/
---
## PdfSaveOptions::get_JpegQuality method


Ottiene o imposta un valore che determina la qualità delle immagini JPEG all'interno del documento PDF.

```cpp
int32_t Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality()
```

## Note


Il valore predefinito è 100.

Questa proprietà è utilizzata in combinazione con l'opzione [ImageCompression](../get_imagecompression/).

Ha effetto solo quando un documento contiene immagini JPEG.

Utilizza questa proprietà per ottenere o impostare la qualità delle immagini all'interno di un documento durante il salvataggio in formato PDF. Il valore può variare da 0 a 100, dove 0 indica la qualità più bassa ma la massima compressione e 100 indica la migliore qualità ma la compressione minima. Se la qualità è 100 e l'immagine di origine è JPEG, significa nessuna compressione: i byte originali verranno salvati.
## Vedi anche

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
