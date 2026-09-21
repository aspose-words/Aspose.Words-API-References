---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias metod"
linktitle: "get_ImagesFolderAlias"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias metod. Anger namnet på den mapp som används för att konstruera bild‑URI:er skrivna i ett HTML‑dokument. Standard är en tom sträng i C++."
type: docs
weight: 39000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_imagesfolderalias/
---
## HtmlSaveOptions::get_ImagesFolderAlias method


Anger namnet på mappen som används för att konstruera bild‑URI:er som skrivs in i ett HTML‑dokument. Standard är en tom sträng.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias() const
```

## Anmärkningar


När du sparar ett [Document](../../../aspose.words/document/) i HTML‑format måste Aspose.Words spara alla bilder som är inbäddade i dokumentet som fristående filer. [ImagesFolder](../get_imagesfolder/) låter dig ange var bilderna ska sparas och [ImagesFolderAlias](./) låter dig ange hur bild‑URI:erna ska konstrueras.

Om [ImagesFolderAlias](./) inte är en tom sträng, kommer bild‑URI:n som skrivs till HTML att bli *ImagesFolderAlias + <image file name>*.

Om [ImagesFolderAlias](./) är en tom sträng, kommer bild‑URI:n som skrivs till HTML att bli *ImagesFolder + <image file name>*.

Om [ImagesFolderAlias](./) är satt till '.' (punkt), kommer bildfilnamnet att skrivas till HTML utan sökväg oavsett andra alternativ.

Ett alternativt sätt att ange namnet på mappen för att konstruera bild‑URI:er är att använda [ResourceFolderAlias](../get_resourcefolderalias/).

## Exempel



Visar hur man ställer in mappar och mapparalias för externa resurser som Aspose.Words kommer att skapa när ett dokument sparas som HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
options->set_ExportFontResources(true);
options->set_ImageResolution(72);
options->set_FontResourcesSubsettingSizeThreshold(0);
options->set_FontsFolder(get_ArtifactsDir() + u"Fonts");
options->set_ImagesFolder(get_ArtifactsDir() + u"Images");
options->set_ResourceFolder(get_ArtifactsDir() + u"Resources");
options->set_FontsFolderAlias(u"http://example.com/fonts");
options->set_ImagesFolderAlias(u"http://example.com/images");
options->set_ResourceFolderAlias(u"http://example.com/resources");
options->set_ExportOriginalUrlForLinkedImages(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.FolderAlias.html", options);
```

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
