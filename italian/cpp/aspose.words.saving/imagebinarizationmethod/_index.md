---
title: "Aspose::Words::Saving::ImageBinarizationMethod enum"
linktitle: "ImageBinarizationMethod"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::ImageBinarizationMethod enum. Specifica il metodo usato per binarizzare l'immagine in C++."
type: docs
weight: 63000
url: /it/cpp/aspose.words.saving/imagebinarizationmethod/
---
## ImageBinarizationMethod enum


Specifica il metodo utilizzato per binarizzare l'immagine.

```cpp
enum class ImageBinarizationMethod
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Threshold | 0 | Specifica il metodo di soglia. |
| FloydSteinbergDithering | 1 | Specifica la dithering usando il metodo di diffusione dell'errore Floyd‑Steinberg. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
