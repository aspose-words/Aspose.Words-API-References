---
title: "Aspose::Words::Saving::ImageSaveOptions::ImageSaveOptions Konstruktor"
linktitle: "ImageSaveOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ImageSaveOptions::ImageSaveOptions Konstruktor. Initialisiert eine neue Instanz dieser Klasse, die zum Speichern gerenderter Bilder im Tiff-, Png-, Bmp-, Jpeg-, Emf-, Eps-, WebP- oder Svg-Format in C++ verwendet werden kann."
type: docs
weight: 2000
url: /de/cpp/aspose.words.saving/imagesaveoptions/imagesaveoptions/
---
## ImageSaveOptions::ImageSaveOptions constructor


Initialisiert eine neue Instanz dieser Klasse, die zum Speichern gerenderter Bilder im [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/), [Eps](../../../aspose.words/saveformat/), [WebP](../) oder [Svg](../../../aspose.words/saveformat/) Format verwendet werden kann.

```cpp
Aspose::Words::Saving::ImageSaveOptions::ImageSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Kann im [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/), [Eps](../../../aspose.words/saveformat/)[WebP](../) oder [Svg](../../../aspose.words/saveformat/) Format sein. |

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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
