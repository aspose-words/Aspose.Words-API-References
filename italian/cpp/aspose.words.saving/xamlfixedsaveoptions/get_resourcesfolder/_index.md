---
title: "Aspose::Words::Saving::XamlFixedSaveOptions::get_ResourcesFolder metodo"
linktitle: "get_ResourcesFolder"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::XamlFixedSaveOptions::get_ResourcesFolder metodo. Specifica la cartella fisica dove le risorse (immagini e caratteri) vengono salvate durante l'esportazione di un documento nel formato Xaml a pagina fissa. Il valore predefinito è null in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.saving/xamlfixedsaveoptions/get_resourcesfolder/
---
## XamlFixedSaveOptions::get_ResourcesFolder method


Specifica la cartella fisica in cui le risorse (immagini e font) vengono salvate durante l'esportazione di un documento nel formato Xaml a pagina fissa. Il valore predefinito è **null**.

```cpp
System::String Aspose::Words::Saving::XamlFixedSaveOptions::get_ResourcesFolder() const
```

## Note


Quando salvi un [Document](../../../aspose.words/document/) in formato Xaml a pagina fissa, Aspose.Words deve salvare tutte le immagini incorporate nel documento come file autonomi. [ResourcesFolder](./) consente di specificare dove verranno salvate le immagini e [ResourcesFolderAlias](../get_resourcesfolderalias/) permette di specificare come verranno costruiti gli URI delle immagini.

Se salvi un documento in un file e fornisci un nome file, Aspose.Words, per impostazione predefinita, salva le immagini nella stessa cartella in cui è salvato il file del documento. Usa [ResourcesFolder](./) per sovrascrivere questo comportamento.

Se salvi un documento in uno stream, Aspose.Words non dispone di una cartella dove salvare le immagini, ma deve comunque salvarle da qualche parte. In questo caso, è necessario specificare una cartella accessibile utilizzando la proprietà [ResourcesFolder](./).

## Vedi anche

* Class [XamlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
