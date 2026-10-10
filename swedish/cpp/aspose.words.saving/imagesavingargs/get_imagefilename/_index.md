---
title: "Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName metod"
linktitle: "get_ImageFileName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName metod. Hämtar eller anger filnamnet (utan sökväg) där bilden kommer att sparas i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.saving/imagesavingargs/get_imagefilename/
---
## ImageSavingArgs::get_ImageFileName method


Hämtar eller anger filnamnet (utan sökväg) där bilden kommer att sparas till.

```cpp
System::String Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName() const
```

## Anmärkningar


Denna egenskap låter dig omdefiniera hur bildfilnamn genereras vid export till HTML.

När händelsen avfyras innehåller denna egenskap filnamnet som genererades av Aspose.Words. Du kan ändra värdet på denna egenskap för att spara bilden i en annan fil. Observera att filnamn måste vara unika.

Aspose.Words genererar automatiskt ett unikt filnamn för varje inbäddad bild när du exporterar till HTML-format. Hur bildfilnamnet genereras beror på om du sparar dokumentet till en fil eller till en ström.

När du sparar ett dokument till en fil ser det genererade bildfilnamnet ut som *%<document base file name>.<image number>.<extension>*.

När du sparar ett dokument till en ström ser det genererade bildfilnamnet ut som *Aspose.Words.<document guid>.<image number>.<extension>*.

[ImageFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the **src** attribute for writing to HTML using the document file name, the [ImagesFolder](../../htmlsaveoptions/get_imagesfolder/) and [ImagesFolderAlias](../../htmlsaveoptions/get_imagesfolderalias/) properties.

## Se även

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
