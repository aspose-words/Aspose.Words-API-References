---
title: "Aspose::Words::Drawing::ImageData::get_ImageSize Methode"
linktitle: "get_ImageSize"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ImageData::get_ImageSize Methode. Ruft die Informationen über Bildgröße und Auflösung in C++ ab."
type: docs
weight: 14000
url: /de/cpp/aspose.words.drawing/imagedata/get_imagesize/
---
## ImageData::get_ImageSize method


Ruft die Informationen zur Bildgröße und Auflösung ab.

```cpp
System::SharedPtr<Aspose::Words::Drawing::ImageSize> Aspose::Words::Drawing::ImageData::get_ImageSize()
```

## Hinweise


Wenn das Bild nur verknüpft und nicht im Dokument gespeichert ist, wird eine Größe von Null zurückgegeben.

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

* Class [ImageSize](../../imagesize/)
* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
