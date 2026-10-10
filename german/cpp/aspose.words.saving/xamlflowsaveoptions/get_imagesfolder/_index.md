---
title: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder Methode"
linktitle: "get_ImagesFolder"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder Methode. Gibt den physischen Ordner an, in dem Bilder beim Export eines Dokuments in das XAML‑Format gespeichert werden. Der Standard ist ein leerer String in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.saving/xamlflowsaveoptions/get_imagesfolder/
---
## XamlFlowSaveOptions::get_ImagesFolder method


Gibt den physischen Ordner an, in dem Bilder beim Export eines Dokuments in das XAML-Format gespeichert werden. Standard ist ein leerer String.

```cpp
System::String Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder() const
```

## Hinweise


Wenn Sie ein [Document](../../../aspose.words/document/) im XAML‑Format speichern, muss Aspose.Words alle im Dokument eingebetteten Bilder als eigenständige Dateien speichern. [ImagesFolder](./) ermöglicht es Ihnen, anzugeben, wo die Bilder gespeichert werden, und [ImagesFolderAlias](../get_imagesfolderalias/) ermöglicht die Angabe, wie die Bild‑URIs erstellt werden.

Wenn Sie ein Dokument in einer Datei speichern und einen Dateinamen angeben, speichert Aspose.Words standardmäßig die Bilder im selben Ordner, in dem die Dokumentdatei gespeichert wird. Verwenden Sie [ImagesFolder](./), um dieses Verhalten zu überschreiben.

Wenn Sie ein Dokument in einen Stream speichern, hat Aspose.Words keinen Ordner, in dem die Bilder gespeichert werden können, muss die Bilder jedoch dennoch irgendwo speichern. In diesem Fall müssen Sie einen zugänglichen Ordner in der Eigenschaft [ImagesFolder](./) angeben oder benutzerdefinierte Streams über den Ereignishandler [ImageSavingCallback](../get_imagesavingcallback/) bereitstellen.

## Siehe auch

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
