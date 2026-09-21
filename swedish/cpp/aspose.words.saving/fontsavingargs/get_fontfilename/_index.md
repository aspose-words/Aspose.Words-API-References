---
title: "Aspose::Words::Saving::FontSavingArgs::get_FontFileName-metod"
linktitle: "get_FontFileName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::FontSavingArgs::get_FontFileName‑metoden. Hämtar eller anger filnamnet (utan sökväg) där teckensnittet kommer att sparas i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.saving/fontsavingargs/get_fontfilename/
---
## FontSavingArgs::get_FontFileName method


Hämtar eller anger filnamnet (utan sökväg) där teckensnittet ska sparas till.

```cpp
System::String Aspose::Words::Saving::FontSavingArgs::get_FontFileName() const
```

## Anmärkningar


Denna egenskap låter dig omdefiniera hur teckensnittets filnamn genereras vid export till HTML.

När händelsen avfyras innehåller denna egenskap filnamnet som genererades av Aspose.Words. Du kan ändra värdet på denna egenskap för att spara teckensnittet i en annan fil. Observera att filnamnen måste vara unika.

Aspose.Words genererar automatiskt ett unikt filnamn för varje inbäddat teckensnitt vid export till HTML‑format. Hur teckensnittets filnamn genereras beror på om du sparar dokumentet till en fil eller till en ström.

När du sparar ett dokument till en fil ser det genererade teckensnittets filnamn ut så här *%<document base file name>.<original file name><optional suffix>.<extension>*.

När du sparar ett dokument till en ström ser det genererade teckensnittets filnamn ut så här *Aspose.Words.<document guid>.<original file name><optional suffix>.<extension>*.

[FontFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name, the [FontsFolder](../../htmlsaveoptions/get_fontsfolder/) and [FontsFolderAlias](../../htmlsaveoptions/get_fontsfolderalias/) properties.

## Se även

* Class [FontSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
