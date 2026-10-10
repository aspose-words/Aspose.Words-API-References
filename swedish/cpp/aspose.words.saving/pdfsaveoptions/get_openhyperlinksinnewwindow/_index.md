---
title: "Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow metod"
linktitle: "get_OpenHyperlinksInNewWindow"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow metod. Hämtar eller anger ett värde som bestämmer om hyperlänkar i den genererade Pdf‑dokumentet tvingas öppnas i ett nytt fönster (eller flik) i en webbläsare i C++."
type: docs
weight: 24000
url: /sv/cpp/aspose.words.saving/pdfsaveoptions/get_openhyperlinksinnewwindow/
---
## PdfSaveOptions::get_OpenHyperlinksInNewWindow method


Hämtar eller anger ett värde som bestämmer om hyperlänkar i utdata‑Pdf‑dokumentet tvingas öppnas i ett nytt fönster (eller flik) i en webbläsare.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow() const
```

## Anmärkningar


Standardvärdet är **false**. När detta värde är inställt på **true** sparas hyperlänkar med JavaScript‑kod. JavaScript‑koden är **app.launchURL(\"URL\", true);**, där **URL** är en hyperlänk.

Observera att om detta alternativ är inställt på **true** kan hyperlänkar inte fungera i vissa PDF‑läsare, t.ex. Chrome, Firefox.

JavaScript‑åtgärder är förbjudna enligt PDF/A‑1, PDF/A‑2 och PDF/A‑3‑efterlevnad. Värdet **false** kommer att användas automatiskt i detta fall.
## Se även

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
