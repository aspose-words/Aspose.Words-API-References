---
title: "Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality metodo"
linktitle: "get_JpegQuality"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality metodo. Ottiene o imposta un valore che determina la qualità delle immagini JPEG all'interno del documento Html in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.saving/fixedpagesaveoptions/get_jpegquality/
---
## FixedPageSaveOptions::get_JpegQuality method


Ottiene o imposta un valore che determina la qualità delle immagini JPEG all'interno del documento Html.

```cpp
int32_t Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality() const
```

## Note


Ha effetto solo quando un documento contiene immagini JPEG.

Utilizzare questa proprietà per ottenere o impostare la qualità delle immagini all'interno di un documento quando si salva in formato pagina fissa. Il valore può variare da 0 a 100, dove 0 indica la qualità più bassa ma la massima compressione e 100 indica la migliore qualità ma la compressione minima.

Il valore predefinito è 95.

## Esempi



Mostra come configurare la compressione durante il salvataggio di un documento come JPEG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo rende il documento in un'immagine.
auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Imposta la proprietà "JpegQuality" a "10" per utilizzare una compressione più forte durante il rendering del documento.
// Ciò ridurrà la dimensione del file del documento, ma l'immagine mostrerà artefatti di compressione più evidenti.
imageOptions->set_JpegQuality(10);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Imposta la proprietà "JpegQuality" a "100" per utilizzare una compressione più debole durante il rendering del documento.
// Ciò migliorerà la qualità dell'immagine a costo di un aumento della dimensione del file.
imageOptions->set_JpegQuality(100);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

## Vedi anche

* Class [FixedPageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
