---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias metodo"
linktitle: "get_ImagesFolderAlias"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias. Specifica il nome della cartella usata per costruire gli URI delle immagini scritti in un documento HTML. Il valore predefinito è una stringa vuota in C++."
type: docs
weight: 39000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_imagesfolderalias/
---
## HtmlSaveOptions::get_ImagesFolderAlias method


Specifica il nome della cartella usata per costruire gli URI delle immagini scritti in un documento HTML. Il valore predefinito è una stringa vuota.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias() const
```

## Note


Quando salvi un [Document](../../../aspose.words/document/) in formato HTML, Aspose.Words deve salvare tutte le immagini incorporate nel documento come file autonomi. [ImagesFolder](../get_imagesfolder/) ti consente di specificare dove verranno salvate le immagini e [ImagesFolderAlias](./) consente di specificare come verranno costruiti gli URI delle immagini.

Se [ImagesFolderAlias](./) non è una stringa vuota, l'URI dell'immagine scritto in HTML sarà *ImagesFolderAlias + <image file name>*.

Se [ImagesFolderAlias](./) è una stringa vuota, l'URI dell'immagine scritto in HTML sarà *ImagesFolder + <image file name>*.

Se [ImagesFolderAlias](./) è impostato a '.' (punto), il nome del file immagine verrà scritto in HTML senza percorso, indipendentemente dalle altre opzioni.

Un modo alternativo per specificare il nome della cartella per costruire gli URI delle immagini è utilizzare [ResourceFolderAlias](../get_resourcefolderalias/).

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
