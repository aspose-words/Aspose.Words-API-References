---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution metodo"
linktitle: "get_ImageResolution"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution metodo. Specifica la risoluzione di output per le immagini durante l'esportazione in HTML, MHTML o EPUB. Il valore predefinito è %96 dpi in C++."
type: docs
weight: 36000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_imageresolution/
---
## HtmlSaveOptions::get_ImageResolution method


Specifica la risoluzione di output per le immagini durante l'esportazione in HTML, MHTML o EPUB. Il valore predefinito è **%96 dpi**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution() const
```

## Note


Questa proprietà influisce sulle immagini raster quando [ScaleImageToShapeSize](../get_scaleimagetoshapesize/) è **true** e influisce sui metafile esportati come immagini raster. Alcune proprietà dell'immagine, come il ritaglio o la rotazione, richiedono il salvataggio di immagini trasformate e, in questo caso, le immagini trasformate vengono create nella risoluzione specificata.

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
