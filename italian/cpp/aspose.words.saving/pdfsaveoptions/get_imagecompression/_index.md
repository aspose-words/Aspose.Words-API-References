---
title: "Metodo Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression"
linktitle: "get_ImageCompression"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression. Specifica il tipo di compressione da utilizzare per tutte le immagini nel documento in C++."
type: docs
weight: 21000
url: /it/cpp/aspose.words.saving/pdfsaveoptions/get_imagecompression/
---
## PdfSaveOptions::get_ImageCompression method


Specifica il tipo di compressione da utilizzare per tutte le immagini nel documento.

```cpp
Aspose::Words::Saving::PdfImageCompression Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression() const
```

## Note


Il valore predefinito è [Auto](../../pdfimagecompression/).

Utilizzando [Jpeg](../../pdfimagecompression/) è possibile controllare la qualità delle immagini nel documento di output tramite la proprietà [JpegQuality](../get_jpegquality/).

Utilizzare [Jpeg](../../pdfimagecompression/) offre la velocità di conversione più rapida rispetto alle prestazioni di altri tipi di compressione, ma in questo caso la compressione JPEG è con perdita.

Utilizzare [Auto](../../pdfimagecompression/) consente di controllare la qualità del Jpeg nel documento di output tramite la proprietà [JpegQuality](../get_jpegquality/), ma per altri formati i dati pixel grezzi vengono estratti e salvati con compressione Flate. Questo caso è più lento rispetto alla conversione Jpeg ma è senza perdita.
## Vedi anche

* Enum [PdfImageCompression](../../pdfimagecompression/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
