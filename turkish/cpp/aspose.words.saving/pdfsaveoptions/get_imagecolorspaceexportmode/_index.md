---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode method"
linktitle: "get_ImageColorSpaceExportMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode yöntemi. C++'ta PDF belgesindeki görüntüler için renk uzayının nasıl seçileceğini belirtir."
type: docs
weight: 20000
url: /tr/cpp/aspose.words.saving/pdfsaveoptions/get_imagecolorspaceexportmode/
---
## PdfSaveOptions::get_ImageColorSpaceExportMode method


PDF belgesindeki görüntüler için renk uzayının nasıl seçileceğini belirtir.

```cpp
Aspose::Words::Saving::PdfImageColorSpaceExportMode Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode() const
```

## Açıklamalar


Varsayılan değer [Auto](../../pdfimagecolorspaceexportmode/)'dır.

Eğer [SimpleCmyk](../../pdfimagecolorspaceexportmode/) değeri belirtilirse, [ImageCompression](../get_imagecompression/) seçeneği yok sayılır ve belge içindeki tüm görüntüler için Flate sıkıştırması kullanılır.

[SimpleCmyk](../../pdfimagecolorspaceexportmode/) value is not supported when saving to PDF/A. [Auto](../../pdfimagecolorspaceexportmode/) value will be used instead. 
## Ayrıca Bakınız

* Enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
