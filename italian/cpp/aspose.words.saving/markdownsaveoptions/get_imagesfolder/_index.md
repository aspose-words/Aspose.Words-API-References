---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder metodo"
linktitle: "get_ImagesFolder"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder metodo. Specifica la cartella fisica in cui le immagini vengono salvate durante l'esportazione di un documento nel formato Markdown. Il valore predefinito è una stringa vuota in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.saving/markdownsaveoptions/get_imagesfolder/
---
## MarkdownSaveOptions::get_ImagesFolder method


Specifica la cartella fisica in cui le immagini vengono salvate durante l'esportazione di un documento nel formato [Markdown](../../../aspose.words/saveformat/). Il valore predefinito è una stringa vuota.

```cpp
System::String Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder() const
```

## Note


Quando si salva un [Document](../../../aspose.words/document/) nel formato [Markdown](../../../aspose.words/saveformat/), Aspose.Words deve salvare tutte le immagini incorporate nel documento come file autonomi. [ImagesFolder](./) consente di specificare dove verranno salvate le immagini.

Se salvi un documento in un file e fornisci un nome file, Aspose.Words, per impostazione predefinita, salva le immagini nella stessa cartella in cui è salvato il file del documento. Usa [ImagesFolder](./) per sovrascrivere questo comportamento.

Se si salva un documento in uno stream, Aspose.Words non dispone di una cartella dove salvare le immagini, ma deve comunque salvarle da qualche parte. In questo caso, è necessario specificare una cartella accessibile nella proprietà [ImagesFolder](./).

Se la cartella specificata da [ImagesFolder](./) non esiste, verrà creata automaticamente.

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
