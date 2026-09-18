---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode Methode"
linktitle: "get_ImageColorSpaceExportMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode Methode. Gibt an, wie der Farbraum für die Bilder im PDF‑Dokument in C++ ausgewählt wird."
type: docs
weight: 20000
url: /de/cpp/aspose.words.saving/pdfsaveoptions/get_imagecolorspaceexportmode/
---
## PdfSaveOptions::get_ImageColorSpaceExportMode method


Gibt an, wie der Farbraum für die Bilder im PDF-Dokument ausgewählt wird.

```cpp
Aspose::Words::Saving::PdfImageColorSpaceExportMode Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode() const
```

## Hinweise


Der Standardwert ist [Auto](../../pdfimagecolorspaceexportmode/).

Wenn der Wert [SimpleCmyk](../../pdfimagecolorspaceexportmode/) angegeben ist, wird die Option [ImageCompression](../get_imagecompression/) ignoriert und für alle Bilder im Dokument wird Flate‑Kompression verwendet.

[SimpleCmyk](../../pdfimagecolorspaceexportmode/) value is not supported when saving to PDF/A. [Auto](../../pdfimagecolorspaceexportmode/) value will be used instead. 
## Siehe auch

* Enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
