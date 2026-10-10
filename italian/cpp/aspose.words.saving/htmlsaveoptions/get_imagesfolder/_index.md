---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder metodo"
linktitle: "get_ImagesFolder"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder metodo. Specifica la cartella fisica in cui le immagini vengono salvate durante l'esportazione di un documento in formato HTML. Il valore predefinito è una stringa vuota in C++."
type: docs
weight: 38000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_imagesfolder/
---
## HtmlSaveOptions::get_ImagesFolder method


Specifica la cartella fisica in cui le immagini vengono salvate durante l'esportazione di un documento in formato HTML. Il valore predefinito è una stringa vuota.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder() const
```

## Note


Quando salvi un [Document](../../../aspose.words/document/) in formato HTML, Aspose.Words deve salvare tutte le immagini incorporate nel documento come file autonomi. [ImagesFolder](./) consente di specificare dove verranno salvate le immagini e [ImagesFolderAlias](../get_imagesfolderalias/) permette di specificare come saranno costruiti gli URI delle immagini.

Se salvi un documento in un file e fornisci un nome file, Aspose.Words, per impostazione predefinita, salva le immagini nella stessa cartella in cui è salvato il file del documento. Usa [ImagesFolder](./) per sovrascrivere questo comportamento.

Se salvi un documento in un flusso, Aspose.Words non dispone di una cartella dove salvare le immagini, ma ha comunque bisogno di salvarle da qualche parte. In questo caso, devi specificare una cartella accessibile nella proprietà [ImagesFolder](./) o fornire flussi personalizzati tramite il gestore di eventi [ImageSavingCallback](../get_imagesavingcallback/).

Se la cartella specificata da [ImagesFolder](./) non esiste, verrà creata automaticamente.

[ResourceFolder](../get_resourcefolder/) is another way to specify a folder where images should be saved.

## Esempi



Mostra come specificare la cartella per memorizzare le immagini collegate dopo il salvataggio in .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// Imposta un'opzione per esportare i campi modulo come testo semplice invece di elementi di input HTML.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## Vedi anche

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
