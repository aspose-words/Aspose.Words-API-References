---
title: "Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality Methode"
linktitle: "get_JpegQuality"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality Methode. Ruft einen Wert ab oder legt ihn fest, der die Qualität der JPEG-Bilder in einem Html-Dokument in C++ bestimmt."
type: docs
weight: 4000
url: /de/cpp/aspose.words.saving/fixedpagesaveoptions/get_jpegquality/
---
## FixedPageSaveOptions::get_JpegQuality method


Ruft einen Wert ab oder legt ihn fest, der die Qualität der JPEG-Bilder in einem Html-Dokument bestimmt.

```cpp
int32_t Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality() const
```

## Hinweise


Wirkt nur, wenn ein Dokument JPEG‑Bilder enthält.

Verwenden Sie diese Eigenschaft, um die Qualität der Bilder in einem Dokument beim Speichern im Fixed‑Page‑Format zu erhalten oder festzulegen. Der Wert kann von 0 bis 100 variieren, wobei 0 die schlechteste Qualität aber maximale Kompression bedeutet und 100 die beste Qualität aber minimale Kompression.

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

* Class [FixedPageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
