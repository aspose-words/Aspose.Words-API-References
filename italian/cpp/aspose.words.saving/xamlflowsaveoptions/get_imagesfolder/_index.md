---
title: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder metodo"
linktitle: "get_ImagesFolder"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder metodo. Specifica la cartella fisica dove le immagini vengono salvate durante l'esportazione di un documento in formato XAML. Il valore predefinito è una stringa vuota in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.saving/xamlflowsaveoptions/get_imagesfolder/
---
## XamlFlowSaveOptions::get_ImagesFolder method


Specifica la cartella fisica dove le immagini vengono salvate durante l'esportazione di un documento nel formato XAML. Il valore predefinito è una stringa vuota.

```cpp
System::String Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder() const
```

## Note


Quando salvi un [Document](../../../aspose.words/document/) in formato XAML, Aspose.Words deve salvare tutte le immagini incorporate nel documento come file autonomi. [ImagesFolder](./) ti consente di specificare dove verranno salvate le immagini e [ImagesFolderAlias](../get_imagesfolderalias/) permette di specificare come verranno costruiti gli URI delle immagini.

Se salvi un documento in un file e fornisci un nome file, Aspose.Words, per impostazione predefinita, salva le immagini nella stessa cartella in cui è salvato il file del documento. Usa [ImagesFolder](./) per sovrascrivere questo comportamento.

Se salvi un documento in un flusso, Aspose.Words non dispone di una cartella dove salvare le immagini, ma ha comunque bisogno di salvarle da qualche parte. In questo caso, devi specificare una cartella accessibile nella proprietà [ImagesFolder](./) o fornire flussi personalizzati tramite il gestore di eventi [ImageSavingCallback](../get_imagesavingcallback/).

## Vedi anche

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
