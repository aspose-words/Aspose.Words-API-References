---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder Methode"
linktitle: "get_ImagesFolder"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder Methode. Gibt den physischen Ordner an, in dem Bilder beim Exportieren eines Dokuments in das Markdown-Format gespeichert werden. Standard ist ein leerer String in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.saving/markdownsaveoptions/get_imagesfolder/
---
## MarkdownSaveOptions::get_ImagesFolder method


Gibt den physischen Ordner an, in dem Bilder beim Exportieren eines Dokuments in das [Markdown](../../../aspose.words/saveformat/) Format gespeichert werden. Standard ist ein leerer String.

```cpp
System::String Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder() const
```

## Hinweise


Wenn Sie ein [Dokument](../../../aspose.words/document/) im [Markdown](../../../aspose.words/saveformat/) Format speichern, muss Aspose.Words alle im Dokument eingebetteten Bilder als eigenständige Dateien speichern. [ImagesFolder](./) ermöglicht es Ihnen, anzugeben, wo die Bilder gespeichert werden.

Wenn Sie ein Dokument in einer Datei speichern und einen Dateinamen angeben, speichert Aspose.Words standardmäßig die Bilder im selben Ordner, in dem die Dokumentdatei gespeichert wird. Verwenden Sie [ImagesFolder](./), um dieses Verhalten zu überschreiben.

Wenn Sie ein Dokument in einen Stream speichern, hat Aspose.Words keinen Ordner, in dem die Bilder gespeichert werden können, muss die Bilder jedoch dennoch irgendwo speichern. In diesem Fall müssen Sie einen zugänglichen Ordner in der [ImagesFolder](./) Eigenschaft angeben.

Wenn der von [ImagesFolder](./) angegebene Ordner nicht existiert, wird er automatisch erstellt.

## Beispiele



Zeigt, wie man den Namen des Ordners angibt, der zum Erstellen von Bild-URIs verwendet wird.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

builder->Writeln(u"Some image below:");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

System::String imagesFolder = System::IO::Path::Combine(get_ArtifactsDir(), u"ImagesDir");
auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
// Verwenden Sie die Eigenschaft "ImagesFolder", um einen Ordner im lokalen Dateisystem zuzuweisen, in den
// Aspose.Words wird alle verknüpften Bilder des Dokuments speichern.
saveOptions->set_ImagesFolder(imagesFolder);
// Verwenden Sie die Eigenschaft "ImagesFolderAlias", um diesen Ordner zu verwenden
// bei der Erstellung von Bild-URIs anstelle des Namens des Bilderordners.
saveOptions->set_ImagesFolderAlias(u"http://example.com/images");

builder->get_Document()->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

## Siehe auch

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
