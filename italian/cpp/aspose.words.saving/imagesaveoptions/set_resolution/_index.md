---
title: "Metodo Aspose::Words::Saving::ImageSaveOptions::set_Resolution"
linktitle: "set_Resolution"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::ImageSaveOptions::set_Resolution. Imposta sia la risoluzione orizzontale che quella verticale per le immagini generate, in punti per pollice in C++."
type: docs
weight: 30000
url: /it/cpp/aspose.words.saving/imagesaveoptions/set_resolution/
---
## ImageSaveOptions::set_Resolution method


Imposta sia la risoluzione orizzontale che quella verticale per le immagini generate, in punti per pollice.

```cpp
void Aspose::Words::Saving::ImageSaveOptions::set_Resolution(float value)
```

## Note


Questa proprietà ha effetto solo quando si salva in formati di immagine raster.

## Esempi



Mostra come specificare una risoluzione durante il rendering di un documento in PNG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo rende il documento in un'immagine.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// Imposta la proprietà "Resolution" a "72" per renderizzare il documento a 72 dpi.
options->set_Resolution(72.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.72dpi.png", options);

// Imposta la proprietà "Resolution" a "300" per renderizzare il documento a 300 dpi.
options->set_Resolution(300.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.300dpi.png", options);
```

## Vedi anche

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
