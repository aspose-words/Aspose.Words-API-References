---
title: "Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod Methode"
linktitle: "get_TiffBinarizationMethod"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod Methode. Ermittelt oder legt die Methode fest, die beim Konvertieren von Bildern in das 1‑bpp‑Format verwendet wird, wenn SaveFormat Tiff ist und TiffCompression gleich Ccitt3 oder Ccitt4 ist, in C++."
type: docs
weight: 16000
url: /de/cpp/aspose.words.saving/imagesaveoptions/get_tiffbinarizationmethod/
---
## ImageSaveOptions::get_TiffBinarizationMethod method


Ermittelt oder legt die Methode fest, die beim Konvertieren von Bildern in das 1‑bpp‑Format verwendet wird, wenn [SaveFormat](../get_saveformat/) [Tiff](../../../aspose.words/saveformat/) ist und [TiffCompression](../get_tiffcompression/) gleich [Ccitt3](../../tiffcompression/) oder [Ccitt4](../../tiffcompression/) ist.

```cpp
Aspose::Words::Saving::ImageBinarizationMethod Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod() const
```

## Hinweise


Der Standardwert ist [Threshold](../../imagebinarizationmethod/).

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

* Enum [ImageBinarizationMethod](../../imagebinarizationmethod/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
