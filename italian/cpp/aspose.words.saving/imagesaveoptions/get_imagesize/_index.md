---
title: "Aspose::Words::Saving::ImageSaveOptions::get_ImageSize metodo"
linktitle: "get_ImageSize"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_ImageSize metodo. Ottiene o imposta la dimensione di un'immagine generata in pixel in C++."
type: docs
weight: 7500
url: /it/cpp/aspose.words.saving/imagesaveoptions/get_imagesize/
---
## ImageSaveOptions::get_ImageSize method


Ottiene o imposta le dimensioni di un'immagine generata in pixel.

```cpp
System::Drawing::Size Aspose::Words::Saving::ImageSaveOptions::get_ImageSize() const
```

## Note


Questa proprietà ha effetto solo quando si salva in formati di immagine raster.

Il valore predefinito è (0 x 0), il che significa che la dimensione dell'immagine generata verrà calcolata in base alla dimensione dell'immagine in punti, alla risoluzione specificata e alla scala.

## Esempi



Mostra come rendere ogni pagina di un documento in un'immagine TIFF separata.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo rende il documento in un'immagine.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);

for (int32_t i = 0; i < doc->get_PageCount(); i++)
{
    // Imposta la proprietà "PageSet" al numero della prima pagina da
    // da cui iniziare a renderizzare il documento.
    options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(i));
    // Esporta la pagina a 2325x5325 pixel e 600 dpi.
    options->set_Resolution(600.0f);
    options->set_ImageSize(System::Drawing::Size(2325, 5325));

    doc->Save(get_ArtifactsDir() + System::String::Format(u"ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
}
```

## Vedi anche

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
