---
title: "Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality metod"
linktitle: "get_JpegQuality"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality metod. Hämtar eller anger ett värde som bestämmer kvaliteten på JPEG‑bilderna i PDF‑dokumentet i C++."
type: docs
weight: 23000
url: /sv/cpp/aspose.words.saving/pdfsaveoptions/get_jpegquality/
---
## PdfSaveOptions::get_JpegQuality method


Hämtar eller anger ett värde som bestämmer kvaliteten på JPEG-bilder i PDF-dokumentet.

```cpp
int32_t Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality()
```

## Anmärkningar


Standardvärdet är 100.

Denna egenskap används tillsammans med alternativet [ImageCompression](../get_imagecompression/).

Har effekt endast när ett dokument innehåller JPEG-bilder.

Använd denna egenskap för att hämta eller ange kvaliteten på bilderna i ett dokument när det sparas i PDF‑format. Värdet kan variera från 0 till 100 där 0 betyder sämst kvalitet men maximal komprimering och 100 betyder bästa kvalitet men minimal komprimering. Om kvaliteten är 100 och källbilden är JPEG innebär det ingen komprimering – de ursprungliga bytena sparas.
## Se även

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
