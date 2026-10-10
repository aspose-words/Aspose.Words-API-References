---
title: "Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod metodo"
linktitle: "get_TiffBinarizationMethod"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod. Ottiene o imposta il metodo usato durante la conversione delle immagini al formato 1 bpp quando SaveFormat è Tiff e TiffCompression è uguale a Ccitt3 o Ccitt4 in C++."
type: docs
weight: 16000
url: /it/cpp/aspose.words.saving/imagesaveoptions/get_tiffbinarizationmethod/
---
## ImageSaveOptions::get_TiffBinarizationMethod method


Ottiene o imposta il metodo usato durante la conversione delle immagini al formato 1 bpp quando [SaveFormat](../get_saveformat/) è [Tiff](../../../aspose.words/saveformat/) e [TiffCompression](../get_tiffcompression/) è uguale a [Ccitt3](../../tiffcompression/) o [Ccitt4](../../tiffcompression/).

```cpp
Aspose::Words::Saving::ImageBinarizationMethod Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod() const
```

## Note


Il valore predefinito è [Threshold](../../imagebinarizationmethod/).

## Esempi



Mostra come impostare la soglia di errore di binarizzazione TIFF quando si utilizza il metodo Floyd‑Steinberg per renderizzare un'immagine TIFF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Quando salviamo il documento come TIFF, possiamo passare un oggetto SaveOptions a
// regolare la dithering che Aspose.Words applicherà durante il rendering di questa immagine.
// Il valore predefinito della proprietà "ThresholdForFloydSteinbergDithering" è 128.
// Valori più alti tendono a produrre immagini più scure.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
options->set_TiffCompression(Aspose::Words::Saving::TiffCompression::Ccitt3);
options->set_TiffBinarizationMethod(Aspose::Words::Saving::ImageBinarizationMethod::FloydSteinbergDithering);
options->set_ThresholdForFloydSteinbergDithering(240);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```

## Vedi anche

* Enum [ImageBinarizationMethod](../../imagebinarizationmethod/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
