---
title: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName metod"
linktitle: "get_ResourceFileName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName metod. Hämtar eller anger filnamnet (utan sökväg) där resursen kommer att sparas i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.saving/resourcesavingargs/get_resourcefilename/
---
## ResourceSavingArgs::get_ResourceFileName method


Hämtar eller anger filnamnet (utan sökväg) där resursen kommer att sparas.

```cpp
System::String Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName() const
```

## Anmärkningar


Denna egenskap låter dig omdefiniera hur resursfilnamn genereras vid export till fastsidig HTML, SVG eller Markdown.

När händelsen utlöses innehåller denna egenskap filnamnet som genererades av Aspose.Words. Du kan ändra värdet på denna egenskap för att spara resursen i en annan fil. Observera att filnamn måste vara unika.

Aspose.Words genererar automatiskt ett unikt filnamn för varje resurs vid export till fastsidig HTML, SVG eller Markdown-format. Hur resursfilnamnet genereras beror på om du sparar dokumentet till en fil eller till en ström.

När du sparar ett dokument till en fil ser det genererade resursfilnamnet ut så här *%<document base file name>.<image number>.<extension>*.

När du sparar ett dokument till en ström ser det genererade resursfilnamnet ut så här *Aspose.Words.<document guid>.<image number>.<extension>*.

[ResourceFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the **src** attribute for writing to fixed page HTML, SVG or Markdown using the document file name, the [ResourcesFolder](../../htmlfixedsaveoptions/get_resourcesfolder/) or [ResourcesFolder](../../svgsaveoptions/get_resourcesfolder/) and [ResourcesFolderAlias](../../htmlfixedsaveoptions/get_resourcesfolderalias/) or [ResourcesFolderAlias](../../svgsaveoptions/get_resourcesfolderalias/) or [ImagesFolder](../../markdownsaveoptions/get_imagesfolder/) or [ImagesFolderAlias](../../markdownsaveoptions/get_imagesfolderalias/) properties.

## Se även

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
