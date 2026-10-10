---
title: "Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality Methode"
linktitle: "get_JpegQuality"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality Methode. Ruft einen Wert ab oder legt ihn fest, der die Qualität der JPEG‑Bilder im PDF‑Dokument bestimmt, in C++."
type: docs
weight: 23000
url: /de/cpp/aspose.words.saving/pdfsaveoptions/get_jpegquality/
---
## PdfSaveOptions::get_JpegQuality method


Liest oder legt einen Wert fest, der die Qualität der JPEG‑Bilder im PDF‑Dokument bestimmt.

```cpp
int32_t Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality()
```

## Hinweise


Der Standardwert ist 100.

Diese Eigenschaft wird zusammen mit der Option [ImageCompression](../get_imagecompression/) verwendet.

Wirkt nur, wenn ein Dokument JPEG‑Bilder enthält.

Verwenden Sie diese Eigenschaft, um die Qualität der Bilder in einem Dokument beim Speichern im PDF‑Format abzurufen oder festzulegen. Der Wert kann von 0 bis 100 variieren, wobei 0 die schlechteste Qualität aber maximale Kompression bedeutet und 100 die beste Qualität aber minimale Kompression. Wenn die Qualität 100 beträgt und das Quellbild ein JPEG ist, bedeutet dies keine Kompression – die Originalbytes werden gespeichert.
## Siehe auch

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
