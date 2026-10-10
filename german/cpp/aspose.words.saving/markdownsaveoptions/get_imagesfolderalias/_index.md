---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias Methode"
linktitle: "get_ImagesFolderAlias"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias Methode. Gibt den Namen des Ordners an, der zum Erstellen von Bild-URIs verwendet wird, die in ein Dokument geschrieben werden. Der Standardwert ist ein leerer String in C++."
type: docs
weight: 5500
url: /de/cpp/aspose.words.saving/markdownsaveoptions/get_imagesfolderalias/
---
## MarkdownSaveOptions::get_ImagesFolderAlias method


Gibt den Namen des Ordners an, der zum Erstellen von Bild-URIs verwendet wird, die in ein Dokument geschrieben werden. Standard ist ein leerer String.

```cpp
System::String Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias() const
```

## Hinweise


Wenn Sie ein [Document](../../../aspose.words/document/) im [Markdown](../../../aspose.words/saveformat/) Format speichern, muss Aspose.Words alle im Dokument eingebetteten Bilder als eigenständige Dateien speichern. [ImagesFolder](../get_imagesfolder/) ermöglicht es Ihnen, anzugeben, wo die Bilder gespeichert werden, und [ImagesFolderAlias](./) ermöglicht die Angabe, wie die Bild-URIs konstruiert werden.

Wenn [ImagesFolderAlias](./) kein leerer String ist, wird die in Markdown geschriebene Bild-URI *ImagesFolderAlias + <image file name>* sein.

Wenn [ImagesFolderAlias](./) ein leerer String ist, wird die in Markdown geschriebene Bild-URI *ImagesFolder + <image file name>* sein.

Wenn [ImagesFolderAlias](./) auf '.' (Punkt) gesetzt ist, wird der Bilddateiname in Markdown ohne Pfad geschrieben, unabhängig von anderen Optionen.

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
