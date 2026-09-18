---
title: "Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName Methode"
linktitle: "get_ImageFileName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName Methode. Ruft den Dateinamen (ohne Pfad) ab oder legt ihn fest, unter dem das Bild in C++ gespeichert wird."
type: docs
weight: 4000
url: /de/cpp/aspose.words.saving/imagesavingargs/get_imagefilename/
---
## ImageSavingArgs::get_ImageFileName method


Liest oder setzt den Dateinamen (ohne Pfad), in dem das Bild gespeichert wird.

```cpp
System::String Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName() const
```

## Hinweise


Diese Eigenschaft ermöglicht es Ihnen, zu definieren, wie die Bilddateinamen beim Export nach HTML erzeugt werden.

Wenn das Ereignis ausgelöst wird, enthält diese Eigenschaft den von Aspose.Words erzeugten Dateinamen. Sie können den Wert dieser Eigenschaft ändern, um das Bild in einer anderen Datei zu speichern. Beachten Sie, dass Dateinamen eindeutig sein müssen.

Aspose.Words erzeugt beim Export in das HTML-Format automatisch einen eindeutigen Dateinamen für jedes eingebettete Bild. Wie der Bilddateiname erzeugt wird, hängt davon ab, ob Sie das Dokument in einer Datei oder in einem Stream speichern.

Beim Speichern eines Dokuments in einer Datei sieht der erzeugte Bilddateiname wie *%<document base file name>.<image number>.<extension>* aus.

Beim Speichern eines Dokuments in einem Stream sieht der erzeugte Bilddateiname wie *Aspose.Words.<document guid>.<image number>.<extension>* aus.

[ImageFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the **src** attribute for writing to HTML using the document file name, the [ImagesFolder](../../htmlsaveoptions/get_imagesfolder/) and [ImagesFolderAlias](../../htmlsaveoptions/get_imagesfolderalias/) properties.

## Siehe auch

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
