---
title: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder metod"
linktitle: "get_ImagesFolder"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder metod. Anger den fysiska mappen där bilder sparas när ett dokument exporteras till XAML‑format. Standard är en tom sträng i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.saving/xamlflowsaveoptions/get_imagesfolder/
---
## XamlFlowSaveOptions::get_ImagesFolder method


Anger den fysiska mappen där bilder sparas när ett dokument exporteras till XAML-format. Standardvärdet är en tom sträng.

```cpp
System::String Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder() const
```

## Anmärkningar


När du sparar ett [Document](../../../aspose.words/document/) i XAML-format måste Aspose.Words spara alla bilder som är inbäddade i dokumentet som fristående filer. [ImagesFolder](./) låter dig ange var bilderna ska sparas och [ImagesFolderAlias](../get_imagesfolderalias/) låter dig ange hur bild-URI:erna ska konstrueras.

Om du sparar ett dokument i en fil och anger ett filnamn sparar Aspose.Words som standard bilderna i samma mapp där dokumentfilen sparas. Använd [ImagesFolder](./) för att åsidosätta detta beteende.

Om du sparar ett dokument i en ström har Aspose.Words ingen mapp att spara bilderna i, men måste ändå spara dem någonstans. I så fall måste du ange en åtkomlig mapp i egenskapen [ImagesFolder](./) eller tillhandahålla anpassade strömmar via händelsehanteraren [ImageSavingCallback](../get_imagesavingcallback/).

## Se även

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
