---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder Methode"
linktitle: "get_ResourcesFolder"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder Methode. Gibt den physischen Ordner an, in dem Ressourcen (Bilder, Schriftarten, CSS) beim Exportieren eines Dokuments in das Html-Format gespeichert werden. Der Standardwert ist null in C++."
type: docs
weight: 15000
url: /de/cpp/aspose.words.saving/htmlfixedsaveoptions/get_resourcesfolder/
---
## HtmlFixedSaveOptions::get_ResourcesFolder method


Gibt den physischen Ordner an, in dem Ressourcen (Bilder, Schriftarten, CSS) beim Export eines Dokuments in das Html-Format gespeichert werden. Standardwert ist **null**.

```cpp
System::String Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder() const
```

## Hinweise


Wirkt nur, wenn die Eigenschaft [ExportEmbeddedImages](../get_exportembeddedimages/) **false** ist.

Wenn Sie ein [Document](../../../aspose.words/document/) im Html-Format speichern, muss Aspose.Words alle im Dokument eingebetteten Bilder als eigenständige Dateien speichern. [ResourcesFolder](./) ermöglicht es Ihnen, anzugeben, wo die Bilder gespeichert werden, und [ResourcesFolderAlias](../get_resourcesfolderalias/) ermöglicht die Angabe, wie die Bild-URIs konstruiert werden.

Wenn Sie ein Dokument in einer Datei speichern und einen Dateinamen angeben, speichert Aspose.Words standardmäßig die Bilder im selben Ordner, in dem die Dokumentdatei gespeichert wird. Verwenden Sie [ResourcesFolder](./), um dieses Verhalten zu überschreiben.

Wenn Sie ein Dokument in einen Stream speichern, hat Aspose.Words keinen Ordner, in dem die Bilder gespeichert werden können, muss die Bilder jedoch trotzdem irgendwo speichern. In diesem Fall müssen Sie einen zugänglichen Ordner mithilfe der Eigenschaft [ResourcesFolder](./) angeben.

## Siehe auch

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
