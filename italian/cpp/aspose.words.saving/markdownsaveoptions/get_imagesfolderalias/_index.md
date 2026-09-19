---
title: "Metodo Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias"
linktitle: "get_ImagesFolderAlias"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias. Specifica il nome della cartella usata per costruire gli URI delle immagini scritti in un documento. Il valore predefinito è una stringa vuota in C++."
type: docs
weight: 5500
url: /it/cpp/aspose.words.saving/markdownsaveoptions/get_imagesfolderalias/
---
## MarkdownSaveOptions::get_ImagesFolderAlias method


Specifica il nome della cartella usata per costruire gli URI delle immagini scritti in un documento. Il valore predefinito è una stringa vuota.

```cpp
System::String Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias() const
```

## Note


Quando salvi un [Document](../../../aspose.words/document/) in formato [Markdown](../../../aspose.words/saveformat/), Aspose.Words deve salvare tutte le immagini incorporate nel documento come file autonomi. [ImagesFolder](../get_imagesfolder/) ti consente di specificare dove verranno salvate le immagini e [ImagesFolderAlias](./) permette di specificare come verranno costruiti gli URI delle immagini.

Se [ImagesFolderAlias](./) non è una stringa vuota, l'URI dell'immagine scritto in Markdown sarà *ImagesFolderAlias + <image file name>*.

Se [ImagesFolderAlias](./) è una stringa vuota, l'URI dell'immagine scritto in Markdown sarà *ImagesFolder + <image file name>*.

Se [ImagesFolderAlias](./) è impostato a '.' (punto), il nome del file immagine verrà scritto in Markdown senza percorso, indipendentemente dalle altre opzioni.

## Esempi



Mostra come specificare il nome della cartella usata per costruire gli URI delle immagini.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

builder->Writeln(u"Some image below:");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

System::String imagesFolder = System::IO::Path::Combine(get_ArtifactsDir(), u"ImagesDir");
auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
// Usa la proprietà "ImagesFolder" per assegnare una cartella nel file system locale in cui
// Aspose.Words salverà tutte le immagini collegate del documento.
saveOptions->set_ImagesFolder(imagesFolder);
// Usa la proprietà "ImagesFolderAlias" per utilizzare questa cartella
// quando si costruiscono gli URI delle immagini invece del nome della cartella delle immagini.
saveOptions->set_ImagesFolderAlias(u"http://example.com/images");

builder->get_Document()->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

## Vedi anche

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
