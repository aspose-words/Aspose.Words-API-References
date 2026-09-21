---
title: "Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts metod"
linktitle: "get_EmbedFullFonts"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts metod. Styr hur teckensnitt bäddas in i de resulterande PDF-dokumenten i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words.saving/pdfsaveoptions/get_embedfullfonts/
---
## PdfSaveOptions::get_EmbedFullFonts method


Styr hur teckensnitt bäddas in i de resulterande PDF-dokumenten.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts() const
```

## Anmärkningar


Standardvärdet är **false**, vilket betyder att teckensnitten delmängdas innan inbäddning. Delmängd är användbart om du vill hålla utdatafilens storlek mindre. Delmängd tar bort alla oanvända glyfer från ett teckensnitt.

När detta värde sätts till **true**, bäddas en komplett teckensnittfil in i PDF utan delmängd. Detta kommer att resultera i större utdatafiler, men kan vara ett användbart alternativ när du vill redigera den resulterande PDF:en senare (t.ex. lägga till mer text).

Vissa teckensnitt är stora (flera megabyte) och att bädda in dem utan delmängd kommer att resultera i stora utdata-dokument.
## Se även

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
