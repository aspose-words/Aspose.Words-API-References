---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages metod"
linktitle: "get_ExportOriginalUrlForLinkedImages"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages metod. Anger om den ursprungliga URL‑en ska användas som URL för de länkade bilderna. Standardvärdet är false i C++."
type: docs
weight: 22000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages method


Anger om den ursprungliga URL:en ska användas som URL för de länkade bilderna. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages() const
```

## Anmärkningar


Om värdet är satt till **true**[SourceFullName](../../../aspose.words.drawing/imagedata/get_sourcefullname/) används värdet som URL för länkade bilder och länkade bilder laddas inte in i dokumentets mapp eller [ImagesFolder](../get_imagesfolder/).

Om värdet är satt till **false** laddas länkade bilder in i dokumentets mapp eller [ImagesFolder](../get_imagesfolder/) och URL för varje länkad bild konstrueras beroende på dokumentets mapp, [ImagesFolder](../get_imagesfolder/) och [ImagesFolderAlias](../get_imagesfolderalias/) egenskaper.

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
