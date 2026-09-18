---
title: "Aspose::Words::Drawing::ImageSize class"
linktitle: "ImageSize"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ImageSize class. Enthält Informationen über Bildgröße und Auflösung. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words.drawing/imagesize/
---
## ImageSize class


Enthält Informationen über Bildgröße und Auflösung. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Images](https://docs.aspose.com/words/cpp/working-with-images/).

```cpp
class ImageSize : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_HeightPixels](./get_heightpixels/)() const | Ermittelt die Höhe des Bildes in Pixeln. |
| [get_HeightPoints](./get_heightpoints/)() | Ermittelt die Höhe des Bildes in Punkten. 1 Punkt entspricht 1/72 Zoll. |
| [get_HorizontalResolution](./get_horizontalresolution/)() const | Ermittelt die horizontale Auflösung in DPI. |
| [get_VerticalResolution](./get_verticalresolution/)() const | Ermittelt die vertikale Auflösung in DPI. |
| [get_WidthPixels](./get_widthpixels/)() const | Ermittelt die Breite des Bildes in Pixeln. |
| [get_WidthPoints](./get_widthpoints/)() | Ermittelt die Breite des Bildes in Punkten. 1 Punkt entspricht 1/72 Zoll. |
| [GetType](./gettype/)() const override |  |
| [ImageSize](./imagesize/)(int32_t, int32_t) | Initialisiert Breite und Höhe mit den angegebenen Werten in Pixeln. Initialisiert die Auflösung auf 96 DPI. |
| [ImageSize](./imagesize/)(int32_t, int32_t, double, double) | Initialisiert Breite, Höhe und Auflösung mit den angegebenen Werten. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man eine Form mit einem Bild skaliert.
```cpp
// Wenn wir ein Bild mit der Methode "InsertImage" einfügen, skaliert der Builder die Form, die das Bild anzeigt, so dass,
// Wenn wir das Dokument mit 100 % Zoom in Microsoft Word anzeigen, zeigt die shape das Bild in seiner tatsächlichen Größe an.
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Ein 400 × 400‑Bild erzeugt ein ImageData‑Objekt mit einer Bildgröße von 300 × 300 pt.
System::SharedPtr<Aspose::Words::Drawing::ImageSize> imageSize = shape->get_ImageData()->get_ImageSize();

ASPOSE_ASSERT_EQ(300.0, imageSize->get_WidthPoints());
ASPOSE_ASSERT_EQ(300.0, imageSize->get_HeightPoints());

// Wenn die Abmessungen einer shape mit den Abmessungen der Bilddaten übereinstimmen,
// dann zeigt die shape das Bild in seiner Originalgröße an.
ASPOSE_ASSERT_EQ(300.0, shape->get_Width());
ASPOSE_ASSERT_EQ(300.0, shape->get_Height());

// Reduzieren Sie die Gesamtabmessung der shape um 50 %.
System::WithLambda::setter_mul_wrap(GETTER_SETTER_LAMBDA_ARGS(shape, Width), 0.5);

// Skalierungsfaktoren gelten gleichzeitig für Breite und Höhe, um die Proportionen der shape beizubehalten.
ASPOSE_ASSERT_EQ(150.0, shape->get_Width());
ASPOSE_ASSERT_EQ(150.0, shape->get_Height());

// Wenn wir die shape ändern, bleibt die Größe der Bilddaten unverändert.
ASPOSE_ASSERT_EQ(300.0, imageSize->get_WidthPoints());
ASPOSE_ASSERT_EQ(300.0, imageSize->get_HeightPoints());

// Wir können die Abmessungen der Bilddaten referenzieren, um eine Skalierung basierend auf der Bildgröße anzuwenden.
shape->set_Width(imageSize->get_WidthPoints() * 1.1);

ASPOSE_ASSERT_EQ(330.0, shape->get_Width());
ASPOSE_ASSERT_EQ(330.0, shape->get_Height());

doc->Save(get_ArtifactsDir() + u"Image.ScaleImage.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
