---
title: "Aspose::Words::Saving::ImageSaveOptions::get_JpegQuality Methode"
linktitle: "get_JpegQuality"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ImageSaveOptions::get_JpegQuality Methode. Gibt einen Wert zurück oder legt ihn fest, der die Qualität der erzeugten JPEG‑Bilder in C++ bestimmt."
type: docs
weight: 8000
url: /de/cpp/aspose.words.saving/imagesaveoptions/get_jpegquality/
---
## ImageSaveOptions::get_JpegQuality method


Liest oder setzt einen Wert, der die Qualität der erzeugten JPEG‑Bilder bestimmt.

```cpp
int32_t Aspose::Words::Saving::ImageSaveOptions::get_JpegQuality()
```

## Hinweise


Wirkt nur beim Speichern in JPEG.

Verwenden Sie diese Eigenschaft, um die Qualität der erzeugten Bilder beim Speichern im JPEG‑Format zu erhalten oder festzulegen. Der Wert kann von 0 bis 100 variieren, wobei 0 die schlechteste Qualität bei maximaler Kompression und 100 die beste Qualität bei minimaler Kompression bedeutet.

Der Standardwert ist 95.

## Beispiele



Zeigt, wie man die Kompression beim Speichern eines Dokuments als JPEG konfiguriert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Erstellen Sie ein "ImageSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
// um die Art und Weise zu ändern, wie diese Methode das Dokument in ein Bild rendert.
auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Setzen Sie die \"JpegQuality\"-Eigenschaft auf \"10\", um bei der Darstellung des Dokuments stärkere Kompression zu verwenden.
// Dies reduziert die Dateigröße des Dokuments, aber das Bild zeigt ausgeprägtere Kompressionsartefakte.
imageOptions->set_JpegQuality(10);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Setzen Sie die \"JpegQuality\"-Eigenschaft auf \"100\", um bei der Darstellung des Dokuments schwächere Kompression zu verwenden.
// Dies verbessert die Bildqualität, jedoch zulasten einer erhöhten Dateigröße.
imageOptions->set_JpegQuality(100);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

## Siehe auch

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
