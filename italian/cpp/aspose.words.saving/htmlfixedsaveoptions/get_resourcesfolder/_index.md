---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder metodo"
linktitle: "get_ResourcesFolder"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder metodo. Specifica la cartella fisica dove le risorse (immagini, caratteri, css) vengono salvate durante l'esportazione di un documento in formato Html. Il valore predefinito è null in C++."
type: docs
weight: 15000
url: /it/cpp/aspose.words.saving/htmlfixedsaveoptions/get_resourcesfolder/
---
## HtmlFixedSaveOptions::get_ResourcesFolder method


Specifica la cartella fisica in cui le risorse (immagini, caratteri, css) vengono salvate durante l'esportazione di un documento in formato Html. Il valore predefinito è **null**.

```cpp
System::String Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder() const
```

## Note


Ha effetto solo se la proprietà [ExportEmbeddedImages](../get_exportembeddedimages/) è **false**.

Quando salvi un [Document](../../../aspose.words/document/) in formato Html, Aspose.Words deve salvare tutte le immagini incorporate nel documento come file autonomi. [ResourcesFolder](./) consente di specificare dove verranno salvate le immagini e [ResourcesFolderAlias](../get_resourcesfolderalias/) permette di specificare come verranno costruiti gli URI delle immagini.

Se salvi un documento in un file e fornisci un nome file, Aspose.Words, per impostazione predefinita, salva le immagini nella stessa cartella in cui è salvato il file del documento. Usa [ResourcesFolder](./) per sovrascrivere questo comportamento.

Se salvi un documento in uno stream, Aspose.Words non dispone di una cartella dove salvare le immagini, ma deve comunque salvarle da qualche parte. In questo caso, è necessario specificare una cartella accessibile utilizzando la proprietà [ResourcesFolder](./).

## Vedi anche

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
