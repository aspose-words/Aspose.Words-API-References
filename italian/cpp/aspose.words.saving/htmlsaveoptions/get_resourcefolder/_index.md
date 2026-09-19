---
title: "Metodo Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolder"
linktitle: "get_ResourceFolder"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolder. Specifica una cartella fisica in cui vengono salvate tutte le risorse come immagini, font e CSS esterni quando un documento viene esportato in HTML. Il valore predefinito è una stringa vuota in C++."
type: docs
weight: 43000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_resourcefolder/
---
## HtmlSaveOptions::get_ResourceFolder method


Specifica una cartella fisica in cui tutte le risorse come immagini, caratteri e CSS esterni vengono salvate quando un documento viene esportato in HTML. Il valore predefinito è una stringa vuota.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolder() const
```

## Note


[ResourceFolder](./) is the simplest way to specify a folder where all resources should be written. Another way is to use individual properties [FontsFolder](../get_fontsfolder/), [ImagesFolder](../get_imagesfolder/), and [CssStyleSheetFileName](../get_cssstylesheetfilename/).

[ResourceFolder](./) has a lower priority than folders specified via [FontsFolder](../get_fontsfolder/), [ImagesFolder](../get_imagesfolder/), and [CssStyleSheetFileName](../get_cssstylesheetfilename/). For example, if both [ResourceFolder](./) and [FontsFolder](../get_fontsfolder/) are specified, fonts will be saved to [FontsFolder](../get_fontsfolder/), while images and CSS will be saved to [ResourceFolder](./).

Se la cartella specificata da [ResourceFolder](./) non esiste, verrà creata automaticamente.

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
