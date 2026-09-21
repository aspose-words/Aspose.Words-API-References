---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution metod"
linktitle: "get_ImageResolution"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution metod. Anger utdataupplösningen för bilder vid export till HTML, MHTML eller EPUB. Standard är %96 dpi i C++."
type: docs
weight: 36000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_imageresolution/
---
## HtmlSaveOptions::get_ImageResolution method


Anger utskriftsupplösningen för bilder när man exporterar till HTML, MHTML eller EPUB. Standard är **%96 dpi**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution() const
```

## Anmärkningar


Denna egenskap påverkar rasterbilder när [ScaleImageToShapeSize](../get_scaleimagetoshapesize/) är **true** och påverkar metafiler som exporteras som rasterbilder. Vissa bildegenskaper såsom beskärning eller rotation kräver att transformerade bilder sparas och i så fall skapas de transformerade bilderna i den angivna upplösningen.

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
