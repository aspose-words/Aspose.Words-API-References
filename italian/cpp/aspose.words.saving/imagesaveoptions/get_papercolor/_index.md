---
title: "Aspose::Words::Saving::ImageSaveOptions::get_PaperColor metodo"
linktitle: "get_PaperColor"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::ImageSaveOptions::get_PaperColor. Ottiene o imposta il colore di sfondo (carta) per le immagini generate. Il valore predefinito è White in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words.saving/imagesaveoptions/get_papercolor/
---
## ImageSaveOptions::get_PaperColor method


Ottiene o imposta il colore di sfondo (carta) per le immagini generate. Il valore predefinito è **White**.

```cpp
System::Drawing::Color Aspose::Words::Saving::ImageSaveOptions::get_PaperColor()
```

## Note


Durante il rendering delle pagine di un documento che specifica il proprio colore di sfondo, il colore di sfondo del documento sovrascriverà il colore specificato da questa proprietà.

## Esempi



Renderizza una pagina di un documento Word in un'immagine con sfondo trasparente o colorato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo rende il documento in un'immagine.
auto imgOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Imposta la proprietà "PaperColor" a un colore trasparente per applicare un trasparente
// sfondo al documento durante il rendering in un'immagine.
imgOptions->set_PaperColor(System::Drawing::Color::get_Transparent());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Imposta la proprietà "PaperColor" a un colore opaco per applicare quel colore
// come sfondo del documento mentre lo rendiamo in un'immagine.
imgOptions->set_PaperColor(System::Drawing::Color::get_LightCoral());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

## Vedi anche

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
