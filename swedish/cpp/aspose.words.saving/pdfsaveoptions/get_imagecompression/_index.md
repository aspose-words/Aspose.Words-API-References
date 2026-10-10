---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression method"
linktitle: "get_ImageCompression"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression‑metod. Anger kompressionstyp som ska användas för alla bilder i dokumentet i C++."
type: docs
weight: 21000
url: /sv/cpp/aspose.words.saving/pdfsaveoptions/get_imagecompression/
---
## PdfSaveOptions::get_ImageCompression method


Anger komprimeringstyp som ska användas för alla bilder i dokumentet.

```cpp
Aspose::Words::Saving::PdfImageCompression Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression() const
```

## Anmärkningar


Standard är [Auto](../../pdfimagecompression/).

Genom att använda [Jpeg](../../pdfimagecompression/) kan du kontrollera kvaliteten på bilder i utdata‑dokumentet via egenskapen [JpegQuality](../get_jpegquality/).

Genom att använda [Jpeg](../../pdfimagecompression/) får du den snabbaste konverteringshastigheten jämfört med prestandan för andra kompressionstyper, men i detta fall finns förlustkomprimering för JPEG.

Genom att använda [Auto](../../pdfimagecompression/) kan du kontrollera kvaliteten på Jpeg i utdata‑dokumentet via egenskapen [JpegQuality](../get_jpegquality/), men för andra format extraheras rå pixeldata och sparas med Flate‑kompression. Detta är långsammare än Jpeg‑konvertering men förlustfritt.
## Se även

* Enum [PdfImageCompression](../../pdfimagecompression/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
