---
title: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias Methode"
linktitle: "get_ImagesFolderAlias"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias Methode. Gibt den Namen des Ordners an, der zum Erstellen von Bild‑URIs verwendet wird, die in ein XAML‑Dokument geschrieben werden. Der Standard ist ein leerer String in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.saving/xamlflowsaveoptions/get_imagesfolderalias/
---
## XamlFlowSaveOptions::get_ImagesFolderAlias method


Gibt den Namen des Ordners an, der zum Erstellen von Bild-URIs verwendet wird, die in ein XAML-Dokument geschrieben werden. Standard ist ein leerer String.

```cpp
System::String Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias() const
```

## Hinweise


Wenn Sie ein [Document](../../../aspose.words/document/) im XAML‑Format speichern, muss Aspose.Words alle im Dokument eingebetteten Bilder als eigenständige Dateien speichern. [ImagesFolder](../get_imagesfolder/) ermöglicht es Ihnen, anzugeben, wo die Bilder gespeichert werden, und [ImagesFolderAlias](./) ermöglicht die Angabe, wie die Bild‑URIs erstellt werden.

Wenn [ImagesFolderAlias](./) kein leerer String ist, wird die in XAML geschriebene Bild‑URI *ImagesFolderAlias + <image file name>* sein.

Wenn [ImagesFolderAlias](./) ein leerer String ist, wird die in XAML geschriebene Bild‑URI *ImagesFolder + <image file name>* sein.

Wenn [ImagesFolderAlias](./) auf '.' (Punkt) gesetzt ist, wird der Bilddateiname in XAML ohne Pfad geschrieben, unabhängig von anderen Optionen.

## Siehe auch

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
