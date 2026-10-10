---
title: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias metod"
linktitle: "get_ImagesFolderAlias"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias metod. Anger namnet på mappen som används för att konstruera bild‑URI:er som skrivs in i ett XAML‑dokument. Standard är en tom sträng i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.saving/xamlflowsaveoptions/get_imagesfolderalias/
---
## XamlFlowSaveOptions::get_ImagesFolderAlias method


Anger namnet på den mapp som används för att konstruera bild‑URI:er som skrivs in i ett XAML-dokument. Standardvärdet är en tom sträng.

```cpp
System::String Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias() const
```

## Anmärkningar


När du sparar ett [Document](../../../aspose.words/document/) i XAML‑format måste Aspose.Words spara alla bilder som är inbäddade i dokumentet som fristående filer. [ImagesFolder](../get_imagesfolder/) låter dig ange var bilderna ska sparas och [ImagesFolderAlias](./) låter dig ange hur bild‑URI:erna ska konstrueras.

Om [ImagesFolderAlias](./) inte är en tom sträng, kommer bild‑URI:n som skrivs till XAML att bli *ImagesFolderAlias + <image file name>*.

Om [ImagesFolderAlias](./) är en tom sträng, kommer bild‑URI:n som skrivs till XAML att bli *ImagesFolder + <image file name>*.

Om [ImagesFolderAlias](./) är satt till '.' (punkt), kommer bildfilens namn att skrivas till XAML utan sökväg oavsett andra alternativ.

## Se även

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
