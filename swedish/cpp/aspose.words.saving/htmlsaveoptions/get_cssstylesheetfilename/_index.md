---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName method"
linktitle: "get_CssStyleSheetFileName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName method. Anger sökvägen och namnet på Cascading Style Sheet (CSS)-filen som skrivs när ett dokument exporteras till HTML. Standard är en tom sträng i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_cssstylesheetfilename/
---
## HtmlSaveOptions::get_CssStyleSheetFileName method


Anger sökvägen och namnet på den Cascading [Style](../../../aspose.words/style/) Sheet (CSS)-filen som skrivs när ett dokument exporteras till HTML. Standard är en tom sträng.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName() const
```

## Anmärkningar


Denna egenskap har endast effekt när ett dokument sparas i HTML-format och ett externt CSS‑stilmall begärs med hjälp av [CssStyleSheetType](../get_cssstylesheettype/).

Om den här egenskapen är tom, sparas CSS-filen i samma mapp och med samma namn som HTML-dokumentet men med ".css"-ändelsen.

Om endast sökväg men inget filnamn anges i den här egenskapen, sparas CSS-filen i den angivna mappen och får samma namn som HTML-dokumentet men med ".css"‑ändelsen.

Om mappen som anges av den här egenskapen inte finns, skapas den automatiskt innan CSS‑filen sparas.

Ett annat sätt att ange en mapp där extern CSS‑fil sparas är att använda [ResourceFolder](../get_resourcefolder/).

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
