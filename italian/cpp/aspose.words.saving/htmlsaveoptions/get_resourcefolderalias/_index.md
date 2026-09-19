---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolderAlias metodo"
linktitle: "get_ResourceFolderAlias"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolderAlias metodo. Specifica il nome della cartella usata per costruire gli URI di tutte le risorse scritte in un documento HTML. Il valore predefinito è una stringa vuota in C++."
type: docs
weight: 44000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_resourcefolderalias/
---
## HtmlSaveOptions::get_ResourceFolderAlias method


Specifica il nome della cartella utilizzata per costruire gli URI di tutte le risorse scritte in un documento HTML. Il valore predefinito è una stringa vuota.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolderAlias() const
```

## Note


[ResourceFolderAlias](./) is the simplest way to specify how URIs for all resource files should be constructed. Same information can be specified for images and fonts separately via [ImagesFolderAlias](../get_imagesfolderalias/) and [FontsFolderAlias](../get_fontsfolderalias/) properties, respectively. However, there is no individual property for CSS.

[ResourceFolderAlias](./) has lower priority than [FontsFolderAlias](../get_fontsfolderalias/) and [ImagesFolderAlias](../get_imagesfolderalias/). For example, if both [ResourceFolderAlias](./) and [FontsFolderAlias](../get_fontsfolderalias/) are specified, fonts' URIs will be constructed using [FontsFolderAlias](../get_fontsfolderalias/), while URIs of images and CSS will be constructed using [ResourceFolderAlias](./).

Se [ResourceFolderAlias](./) è vuoto, il valore della proprietà [ResourceFolder](../get_resourcefolder/) verrà usato per costruire gli URI delle risorse.

Se [ResourceFolderAlias](./) è impostato su '.' (punto), gli URI delle risorse conterranno solo i nomi dei file, senza alcun percorso.

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
