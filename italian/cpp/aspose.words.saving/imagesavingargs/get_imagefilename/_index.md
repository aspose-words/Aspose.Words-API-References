---
title: "Metodo Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName"
linktitle: "get_ImageFileName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName. Ottiene o imposta il nome file (senza percorso) in cui l'immagine verrà salvata in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.saving/imagesavingargs/get_imagefilename/
---
## ImageSavingArgs::get_ImageFileName method


Ottiene o imposta il nome file (senza percorso) dove l'immagine verrà salvata.

```cpp
System::String Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName() const
```

## Note


Questa proprietà consente di ridefinire come vengono generati i nomi dei file immagine durante l'esportazione in HTML.

Quando l'evento viene generato, questa proprietà contiene il nome file generato da Aspose.Words. È possibile modificare il valore di questa proprietà per salvare l'immagine in un file diverso. Nota che i nomi dei file devono essere univoci.

Aspose.Words genera automaticamente un nome file univoco per ogni immagine incorporata durante l'esportazione in formato HTML. Il modo in cui il nome del file immagine viene generato dipende dal fatto che il documento venga salvato su un file o su un flusso.

Quando si salva un documento su un file, il nome file immagine generato appare così *%<document base file name>.<image number>.<extension>*.

Quando si salva un documento su un flusso, il nome file immagine generato appare così *Aspose.Words.<document guid>.<image number>.<extension>*.

[ImageFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the **src** attribute for writing to HTML using the document file name, the [ImagesFolder](../../htmlsaveoptions/get_imagesfolder/) and [ImagesFolderAlias](../../htmlsaveoptions/get_imagesfolderalias/) properties.

## Vedi anche

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
