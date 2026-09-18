---
title: "Aspose::Words::Drawing::ImageSize::get_HeightPixels Methode"
linktitle: "get_HeightPixels"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ImageSize::get_HeightPixels method. Gibt die Höhe des Bildes in Pixeln in C++ zurück."
type: docs
weight: 3000
url: /de/cpp/aspose.words.drawing/imagesize/get_heightpixels/
---
## ImageSize::get_HeightPixels method


Ermittelt die Höhe des Bildes in Pixeln.

```cpp
int32_t Aspose::Words::Drawing::ImageSize::get_HeightPixels() const
```


## Beispiele



Zeigt, wie man die Eigenschaften eines Bildes in einer Form liest.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie eine Form in das Dokument ein, die ein Bild aus unserem lokalen Dateisystem enthält.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Wenn die Form ein Bild enthält, ist ihre ImageData-Eigenschaft gültig,
// und sie wird ein ImageSize-Objekt enthalten.
System::SharedPtr<Aspose::Words::Drawing::ImageSize> imageSize = shape->get_ImageData()->get_ImageSize();

// Das ImageSize-Objekt enthält schreibgeschützte Informationen über das Bild innerhalb der Form.
ASSERT_EQ(400, imageSize->get_HeightPixels());
ASSERT_EQ(400, imageSize->get_WidthPixels());

const double delta = 0.05;
ASSERT_NEAR(95.98, imageSize->get_HorizontalResolution(), delta);
ASSERT_NEAR(95.98, imageSize->get_VerticalResolution(), delta);

// Wir können die Größe der Form anhand der Größe ihres Bildes festlegen, um ein Dehnen des Bildes zu vermeiden.
shape->set_Width(imageSize->get_WidthPoints() * 2);
shape->set_Height(imageSize->get_HeightPoints() * 2);

doc->Save(get_ArtifactsDir() + u"Drawing.ImageSize.docx");
```

## Siehe auch

* Class [ImageSize](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
