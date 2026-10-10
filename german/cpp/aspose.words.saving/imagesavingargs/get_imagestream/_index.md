---
title: "Aspose::Words::Saving::ImageSavingArgs::get_ImageStream Methode"
linktitle: "get_ImageStream"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ImageSavingArgs::get_ImageStream Methode. Ermöglicht die Angabe des Streams, in dem das Bild in C++ gespeichert wird."
type: docs
weight: 5000
url: /de/cpp/aspose.words.saving/imagesavingargs/get_imagestream/
---
## ImageSavingArgs::get_ImageStream method


Ermöglicht die Angabe des Streams, in dem das Bild gespeichert wird.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::ImageSavingArgs::get_ImageStream() const
```

## Hinweise


Diese Eigenschaft ermöglicht es Ihnen, Bilder während HTML in Streams statt in Dateien zu speichern.

Der Standardwert ist **null**. Wenn diese Eigenschaft **null** ist, wird das Bild in einer Datei gespeichert, die in der [ImageFileName](../get_imagefilename/) Eigenschaft angegeben ist.

Mit [IImageSavingCallback](../../iimagesavingcallback/) können Sie ein Bild nicht durch ein anderes ersetzen. Es dient ausschließlich zur Steuerung des Speicherorts von Bildern.

## Siehe auch

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
