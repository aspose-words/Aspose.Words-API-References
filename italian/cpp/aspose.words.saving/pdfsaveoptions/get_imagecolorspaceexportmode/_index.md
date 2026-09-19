---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode method"
linktitle: "get_ImageColorSpaceExportMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode method. Specifica come lo spazio colore verrà selezionato per le immagini nel documento PDF in C++."
type: docs
weight: 20000
url: /it/cpp/aspose.words.saving/pdfsaveoptions/get_imagecolorspaceexportmode/
---
## PdfSaveOptions::get_ImageColorSpaceExportMode method


Specifica come verrà selezionato lo spazio colore per le immagini nel documento PDF.

```cpp
Aspose::Words::Saving::PdfImageColorSpaceExportMode Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode() const
```

## Note


Il valore predefinito è [Auto](../../pdfimagecolorspaceexportmode/).

Se viene specificato il valore [SimpleCmyk](../../pdfimagecolorspaceexportmode/), l'opzione [ImageCompression](../get_imagecompression/) viene ignorata e la compressione Flate viene utilizzata per tutte le immagini nel documento.

[SimpleCmyk](../../pdfimagecolorspaceexportmode/) value is not supported when saving to PDF/A. [Auto](../../pdfimagecolorspaceexportmode/) value will be used instead. 
## Vedi anche

* Enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
