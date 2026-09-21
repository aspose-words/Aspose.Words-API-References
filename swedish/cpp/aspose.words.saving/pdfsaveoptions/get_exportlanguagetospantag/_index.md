---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag metod"
linktitle: "get_ExportLanguageToSpanTag"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag metod. Hämtar eller anger ett värde som bestämmer om ett \\\"Span\\\"-tagg ska skapas i dokumentstrukturen för att exportera textens språk i C++."
type: docs
weight: 17000
url: /sv/cpp/aspose.words.saving/pdfsaveoptions/get_exportlanguagetospantag/
---
## PdfSaveOptions::get_ExportLanguageToSpanTag method


Hämtar eller anger ett värde som bestämmer om ett \"Span\"-tagg ska skapas i dokumentstrukturen för att exportera textspråket eller inte.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag() const
```

## Anmärkningar


Standardvärdet är **false** och \"Lang\"-attributet bifogas till en markerad innehållssekvens i en sidström.

När värdet är **true** skapas ett \"Span\"-tagg för texten med icke‑standard språk och \"Lang\"-attributet bifogas till detta tagg.

Detta värde ignoreras när [ExportDocumentStructure](../get_exportdocumentstructure/) är **false**.
## Se även

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
