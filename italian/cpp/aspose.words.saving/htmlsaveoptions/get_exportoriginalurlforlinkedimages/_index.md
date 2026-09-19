---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages metodo"
linktitle: "get_ExportOriginalUrlForLinkedImages"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages metodo. Specifica se l'URL originale deve essere usato come URL delle immagini collegate. Il valore predefinito è false in C++."
type: docs
weight: 22000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages method


Specifica se l'URL originale deve essere utilizzato come URL delle immagini collegate. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages() const
```

## Note


Se il valore è impostato su **true**[SourceFullName](../../../aspose.words.drawing/imagedata/get_sourcefullname/) il valore è usato come URL delle immagini collegate e le immagini collegate non vengono caricate nella cartella del documento o in [ImagesFolder](../get_imagesfolder/).

Se il valore è impostato su **false** le immagini collegate vengono caricate nella cartella del documento o in [ImagesFolder](../get_imagesfolder/) e l'URL di ciascuna immagine collegata viene costruito in base alla cartella del documento, [ImagesFolder](../get_imagesfolder/) e alle proprietà [ImagesFolderAlias](../get_imagesfolderalias/).

## Esempi



Mostra come impostare cartelle e alias di cartelle per le risorse salvate esternamente che Aspose.Words creerà durante il salvataggio di un documento in HTML.
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

## Vedi anche

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
