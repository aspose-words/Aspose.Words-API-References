---
title: "Metodo Aspose::Words::Saving::ImageSavingArgs::get_ImageStream"
linktitle: "get_ImageStream"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::ImageSavingArgs::get_ImageStream. Consente di specificare il flusso in cui l'immagine verrà salvata in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.saving/imagesavingargs/get_imagestream/
---
## ImageSavingArgs::get_ImageStream method


Consente di specificare lo stream dove l'immagine verrà salvata.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::ImageSavingArgs::get_ImageStream() const
```

## Note


Questa proprietà consente di salvare le immagini in stream invece che in file durante l'HTML.

Il valore predefinito è **null**. Quando questa proprietà è **null**, l'immagine verrà salvata in un file specificato nella proprietà [ImageFileName](../get_imagefilename/).

Utilizzando [IImageSavingCallback](../../iimagesavingcallback/) non è possibile sostituire un'immagine con un'altra. È destinato solo al controllo della posizione in cui salvare le immagini.

## Vedi anche

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
