---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias metodo"
linktitle: "get_FontsFolderAlias"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias metodo. Specifica il nome della cartella usata per costruire gli URI dei font scritti in un documento HTML. Il valore predefinito è una stringa vuota in C++."
type: docs
weight: 34000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_fontsfolderalias/
---
## HtmlSaveOptions::get_FontsFolderAlias method


Specifica il nome della cartella usata per costruire gli URI dei caratteri scritti in un documento HTML. Il valore predefinito è una stringa vuota.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias() const
```

## Note


Quando salvi un [Document](../../../aspose.words/document/) in formato HTML e [ExportFontResources](../get_exportfontresources/) è impostato su **true**, Aspose.Words deve salvare i font utilizzati nel documento come file autonomi. [FontsFolder](../get_fontsfolder/) ti consente di specificare dove verranno salvati i font e [FontsFolderAlias](./) consente di specificare come verranno costruiti gli URI dei font.

Se [FontsFolderAlias](./) non è una stringa vuota, l'URI del font scritto in HTML sarà *FontsFolderAlias + <font file name>*.

Se [FontsFolderAlias](./) è una stringa vuota, l'URI del font scritto in HTML sarà *FontsFolder + <font file name>*.

Se [FontsFolderAlias](./) è impostato su '.' (punto), il nome del file del font verrà scritto in HTML senza percorso, indipendentemente dalle altre opzioni.

Un modo alternativo per specificare il nome della cartella per costruire gli URI dei font è utilizzare [ResourceFolderAlias](../get_resourcefolderalias/).

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
