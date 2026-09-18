---
title: "Aspose::Words::Saving::ImageBinarizationMethod enum"
linktitle: "ImageBinarizationMethod"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ImageBinarizationMethod enum. Gibt die Methode an, die zum Binarisieren von Bildern in C++ verwendet wird."
type: docs
weight: 63000
url: /de/cpp/aspose.words.saving/imagebinarizationmethod/
---
## ImageBinarizationMethod enum


Gibt die Methode an, die zum Binärisieren von Bildern verwendet wird.

```cpp
enum class ImageBinarizationMethod
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Threshold | 0 | Gibt die Schwellenwertmethode an. |
| FloydSteinbergDithering | 1 | Gibt das Dithering unter Verwendung der Floyd‑Steinberg-Fehlerdiffusionsmethode an. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
