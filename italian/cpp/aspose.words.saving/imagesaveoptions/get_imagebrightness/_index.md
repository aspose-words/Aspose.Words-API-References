---
title: "Aspose::Words::Saving::ImageSaveOptions::get_ImageBrightness metodo"
linktitle: "get_ImageBrightness"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_ImageBrightness metodo. Ottiene o imposta la luminosità per le immagini generate in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.saving/imagesaveoptions/get_imagebrightness/
---
## ImageSaveOptions::get_ImageBrightness method


Ottiene o imposta la luminosità per le immagini generate.

```cpp
float Aspose::Words::Saving::ImageSaveOptions::get_ImageBrightness() const
```

## Note


Questa proprietà ha effetto solo quando si salva in formati di immagine raster.

Il valore predefinito è 0,5. Il valore deve essere compreso nell'intervallo tra 0 e 1.

## Esempi



Mostra come modificare l'immagine mentre Aspose.Words converte un documento in una.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Quando salviamo il documento come immagine, possiamo passare un oggetto SaveOptions a
// modifica l'immagine mentre l'operazione di salvataggio la rende.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Possiamo regolare queste proprietà per modificare la luminosità e il contrasto dell'immagine.
// Entrambe sono su una scala da 0 a 1 e sono impostate a 0.5 per impostazione predefinita.
options->set_ImageBrightness(0.3f);
options->set_ImageContrast(0.7f);
// Possiamo regolare la risoluzione orizzontale e verticale con queste proprietà.
// Ciò influenzerà le dimensioni dell'immagine.
// Il valore predefinito per queste proprietà è 96.0, per una risoluzione di 96dpi.
options->set_HorizontalResolution(72.f);
options->set_VerticalResolution(72.f);
// Possiamo ridimensionare l'immagine usando questa proprietà. Il valore predefinito è 1.0, per una scala del 100%.
// Possiamo usare questa proprietà per annullare eventuali modifiche alle dimensioni dell'immagine che il cambiamento della risoluzione potrebbe causare.
options->set_Scale(96.f / 72.f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.EditImage.png", options);
```

## Vedi anche

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
