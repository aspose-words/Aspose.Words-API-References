---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder metodo"
linktitle: "get_FontsFolder"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder metodo. Specifica la cartella fisica in cui i font vengono salvati durante l'esportazione di un documento in HTML. Il valore predefinito è una stringa vuota in C++."
type: docs
weight: 33000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_fontsfolder/
---
## HtmlSaveOptions::get_FontsFolder method


Specifica la cartella fisica in cui i caratteri vengono salvati durante l'esportazione di un documento in HTML. Il valore predefinito è una stringa vuota.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder() const
```

## Note


Quando salvi un [Document](../../../aspose.words/document/) in formato HTML e [ExportFontResources](../get_exportfontresources/) è impostato su **true**, Aspose.Words deve salvare i font utilizzati nel documento come file autonomi. [FontsFolder](./) ti consente di specificare dove verranno salvati i font e [FontsFolderAlias](../get_fontsfolderalias/) consente di specificare come verranno costruiti gli URI dei font.

Se salvi un documento in un file e fornisci un nome file, Aspose.Words, per impostazione predefinita, salva i font nella stessa cartella in cui è salvato il file del documento. Usa [FontsFolder](./) per sovrascrivere questo comportamento.

Se salvi un documento in uno stream, Aspose.Words non dispone di una cartella dove salvare i font, ma deve comunque salvarli da qualche parte. In questo caso, è necessario specificare una cartella accessibile nella proprietà [FontsFolder](./) o fornire stream personalizzati tramite il gestore eventi [FontSavingCallback](../get_fontsavingcallback/).

Se la cartella specificata da [FontsFolder](./) non esiste, verrà creata automaticamente.

[ResourceFolder](../get_resourcefolder/) is another way to specify a folder where fonts should be saved.

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
