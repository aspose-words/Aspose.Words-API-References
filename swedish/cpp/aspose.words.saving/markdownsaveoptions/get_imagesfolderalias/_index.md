---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias‑metod"
linktitle: "get_ImagesFolderAlias"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias‑metod. Anger namnet på den mapp som används för att konstruera bild‑URI:er som skrivs in i ett dokument. Standard är en tom sträng i C++."
type: docs
weight: 5500
url: /sv/cpp/aspose.words.saving/markdownsaveoptions/get_imagesfolderalias/
---
## MarkdownSaveOptions::get_ImagesFolderAlias method


Anger namnet på mappen som används för att konstruera bild-URI:er som skrivs in i ett dokument. Standard är en tom sträng.

```cpp
System::String Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias() const
```

## Anmärkningar


När du sparar ett [Document](../../../aspose.words/document/) i [Markdown](../../../aspose.words/saveformat/)‑format måste Aspose.Words spara alla inbäddade bilder i dokumentet som fristående filer. [ImagesFolder](../get_imagesfolder/) låter dig ange var bilderna ska sparas och [ImagesFolderAlias](./) låter dig ange hur bild‑URI:erna ska konstrueras.

Om [ImagesFolderAlias](./) inte är en tom sträng, kommer bild‑URI:n som skrivs till Markdown att bli *ImagesFolderAlias + <image file name>*.

Om [ImagesFolderAlias](./) är en tom sträng, kommer bild‑URI:n som skrivs till Markdown att bli *ImagesFolder + <image file name>*.

Om [ImagesFolderAlias](./) är satt till '.' (punkt), kommer bildfilens namn att skrivas till Markdown utan sökväg oavsett andra alternativ.

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
