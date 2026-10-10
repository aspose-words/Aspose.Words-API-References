---
title: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName metodo"
linktitle: "get_ResourceFileName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName metodo. Ottiene o imposta il nome del file (senza percorso) dove la risorsa verrà salvata in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.saving/resourcesavingargs/get_resourcefilename/
---
## ResourceSavingArgs::get_ResourceFileName method


Ottiene o imposta il nome del file (senza percorso) in cui la risorsa verrà salvata.

```cpp
System::String Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName() const
```

## Note


Questa proprietà consente di ridefinire come vengono generati i nomi dei file di risorsa durante l'esportazione in HTML a pagina fissa, SVG o Markdown.

Quando l'evento viene attivato, questa proprietà contiene il nome del file generato da Aspose.Words. È possibile modificare il valore di questa proprietà per salvare la risorsa in un file diverso. Nota che i nomi dei file devono essere unici.

Aspose.Words genera automaticamente un nome file univoco per ogni risorsa durante l'esportazione in formato HTML a pagina fissa, SVG o Markdown. Il modo in cui il nome del file di risorsa viene generato dipende dal fatto che il documento venga salvato su un file o su uno stream.

Quando si salva un documento su un file, il nome del file di risorsa generato ha l'aspetto *%<document base file name>.<image number>.<extension>*.

Quando si salva un documento su uno stream, il nome del file di risorsa generato ha l'aspetto *Aspose.Words.<document guid>.<image number>.<extension>*.

[ResourceFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the **src** attribute for writing to fixed page HTML, SVG or Markdown using the document file name, the [ResourcesFolder](../../htmlfixedsaveoptions/get_resourcesfolder/) or [ResourcesFolder](../../svgsaveoptions/get_resourcesfolder/) and [ResourcesFolderAlias](../../htmlfixedsaveoptions/get_resourcesfolderalias/) or [ResourcesFolderAlias](../../svgsaveoptions/get_resourcesfolderalias/) or [ImagesFolder](../../markdownsaveoptions/get_imagesfolder/) or [ImagesFolderAlias](../../markdownsaveoptions/get_imagesfolderalias/) properties.

## Vedi anche

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
