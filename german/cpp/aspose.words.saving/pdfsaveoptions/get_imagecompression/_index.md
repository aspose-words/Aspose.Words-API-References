---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression Methode"
linktitle: "get_ImageCompression"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression-Methode. Gibt den Kompressionstyp an, der für alle Bilder im Dokument in C++ verwendet wird."
type: docs
weight: 21000
url: /de/cpp/aspose.words.saving/pdfsaveoptions/get_imagecompression/
---
## PdfSaveOptions::get_ImageCompression method


Gibt den Kompressionstyp an, der für alle Bilder im Dokument verwendet wird.

```cpp
Aspose::Words::Saving::PdfImageCompression Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression() const
```

## Hinweise


Standard ist [Auto](../../pdfimagecompression/).

Durch die Verwendung von [Jpeg](../../pdfimagecompression/) können Sie die Qualität der Bilder im Ausgabedokument über die Eigenschaft [JpegQuality](../get_jpegquality/) steuern.

Die Verwendung von [Jpeg](../../pdfimagecompression/) bietet die schnellste Konvertierungsgeschwindigkeit im Vergleich zur Leistung anderer Kompressionstypen, jedoch liegt in diesem Fall eine verlustbehaftete JPEG-Kompression vor.

Durch die Verwendung von [Auto](../../pdfimagecompression/) können Sie die Qualität von Jpeg im Ausgabedokument über die Eigenschaft [JpegQuality](../get_jpegquality/) steuern, aber für andere Formate werden Rohpixeldaten extrahiert und mit Flate-Kompression gespeichert. Dieser Vorgang ist langsamer als die Jpeg-Konvertierung, jedoch verlustfrei.
## Siehe auch

* Enum [PdfImageCompression](../../pdfimagecompression/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
