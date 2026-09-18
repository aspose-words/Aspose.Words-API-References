---
title: "Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering Methode"
linktitle: "get_ThresholdForFloydSteinbergDithering"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering Methode. Gibt den Schwellenwert zurück oder legt ihn fest, der den Wert des Binärisierungsfehlers in der Floyd‑Steinberg‑Methode bestimmt, wenn ImageBinarizationMethod in C++ auf FloydSteinbergDithering gesetzt ist."
type: docs
weight: 15000
url: /de/cpp/aspose.words.saving/imagesaveoptions/get_thresholdforfloydsteinbergdithering/
---
## ImageSaveOptions::get_ThresholdForFloydSteinbergDithering method


Gibt den Schwellenwert zurück oder legt ihn fest, der den Wert des Binärisierungsfehlers in der Floyd‑Steinberg‑Methode bestimmt, wenn [ImageBinarizationMethod](../../imagebinarizationmethod/) [FloydSteinbergDithering](../../imagebinarizationmethod/) ist.

```cpp
uint8_t Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering() const
```

## Hinweise


Der Standardwert ist 128.

## Beispiele



Zeigt, wie der Fehler‑Schwellenwert für die TIFF‑Binarisierung festgelegt wird, wenn die Floyd‑Steinberg‑Methode zum Rendern eines TIFF‑Bildes verwendet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Wenn wir das Dokument als TIFF speichern, können wir ein SaveOptions‑Objekt übergeben, um
// das Dithering anzupassen, das Aspose.Words beim Rendern dieses Bildes anwenden wird.
// Der Standardwert der Eigenschaft "ThresholdForFloydSteinbergDithering" ist 128.
// Höhere Werte führen tendenziell zu dunkleren Bildern.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
options->set_TiffCompression(Aspose::Words::Saving::TiffCompression::Ccitt3);
options->set_TiffBinarizationMethod(Aspose::Words::Saving::ImageBinarizationMethod::FloydSteinbergDithering);
options->set_ThresholdForFloydSteinbergDithering(240);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```

## Siehe auch

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
