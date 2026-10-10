---
title: "Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName‑metoden"
linktitle: "get_DocumentPartFileName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName metod. Hämtar eller anger filnamnet (utan sökväg) där dokumentdelen kommer att sparas i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.saving/documentpartsavingargs/get_documentpartfilename/
---
## DocumentPartSavingArgs::get_DocumentPartFileName method


Hämtar eller anger filnamnet (utan sökväg) där dokumentdelen ska sparas.

```cpp
System::String Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName() const
```

## Anmärkningar


Denna egenskap låter dig omdefiniera hur filnamnen för dokumentdelen genereras vid export till HTML eller EPUB.

När återanropet utlöses innehåller denna egenskap filnamnet som genererades av Aspose.Words. Du kan ändra värdet på denna egenskap för att spara dokumentdelen i en annan fil. Observera att filnamnet för varje del måste vara unikt.

[DocumentPartFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name. If output document file name was not specified, for instance when saving to a stream, this file name is used only for referencing document parts. The same is true when saving to EPUB format.

## Se även

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
