---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder metod"
linktitle: "get_ImagesFolder"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder metod. Anger den fysiska mappen där bilder sparas när ett dokument exporteras till Markdown-format. Standardvärdet är en tom sträng i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.saving/markdownsaveoptions/get_imagesfolder/
---
## MarkdownSaveOptions::get_ImagesFolder method


Anger den fysiska mappen där bilder sparas när ett dokument exporteras till [Markdown](../../../aspose.words/saveformat/) formatet. Standardvärdet är en tom sträng.

```cpp
System::String Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder() const
```

## Anmärkningar


När du sparar ett [Dokument](../../../aspose.words/document/) i [Markdown](../../../aspose.words/saveformat/) format, måste Aspose.Words spara alla bilder som är inbäddade i dokumentet som fristående filer. [ImagesFolder](./) låter dig ange var bilderna ska sparas.

Om du sparar ett dokument i en fil och anger ett filnamn sparar Aspose.Words som standard bilderna i samma mapp där dokumentfilen sparas. Använd [ImagesFolder](./) för att åsidosätta detta beteende.

Om du sparar ett dokument till en ström har Aspose.Words ingen mapp att spara bilderna i, men måste ändå spara bilderna någonstans. I detta fall måste du ange en åtkomlig mapp i egenskapen [ImagesFolder](./).

Om mappen som anges av [ImagesFolder](./) inte finns kommer den att skapas automatiskt.

## Exempel



Visar hur man anger namnet på den mapp som används för att konstruera bild‑URI:er.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

builder->Writeln(u"Some image below:");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

System::String imagesFolder = System::IO::Path::Combine(get_ArtifactsDir(), u"ImagesDir");
auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
// Använd egenskapen "ImagesFolder" för att tilldela en mapp i det lokala filsystemet som
// Aspose.Words kommer att spara alla dokumentets länkade bilder.
saveOptions->set_ImagesFolder(imagesFolder);
// Använd egenskapen "ImagesFolderAlias" för att använda denna mapp
// vid konstruktion av bild‑URI:er istället för mappens namn.
saveOptions->set_ImagesFolderAlias(u"http://example.com/images");

builder->get_Document()->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

## Se även

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
