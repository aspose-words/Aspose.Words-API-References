---
title: "Aspose::Words::Drawing::ShapeBase::get_Width Methode"
linktitle: "get_Width"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_Width Methode. Ruft die Breite des enthaltenden Blocks der Form ab oder legt sie fest in C++."
type: docs
weight: 54000
url: /de/cpp/aspose.words.drawing/shapebase/get_width/
---
## ShapeBase::get_Width method


Ruft die Breite des enthaltenden Blocks der Form ab oder legt sie fest.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Width()
```

## Hinweise


Für eine Form auf oberster Ebene ist der Wert in Punkten.

Für Formen in einer Gruppe ist der Wert im Koordinatenraum und in den Einheiten der übergeordneten Gruppe.

Der Standardwert ist 0.

## Beispiele



Zeigt, wie man ein schwebendes Bild einfügt und seine Position und Größe festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Konfigurieren Sie die Eigenschaft \"RelativeHorizontalPosition\" der Form, damit der Wert der Eigenschaft \"Left\"
// als der horizontale Abstand der Form, in Punkten, von der linken Seite der Seite.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);

// Setzen Sie den horizontalen Abstand der Form von der linken Seite der Seite auf 100.
shape->set_Left(100);

// Verwenden Sie die Eigenschaft \"RelativeVerticalPosition\" auf ähnliche Weise, um die Form 80pt unterhalb des oberen Seitenrandes zu positionieren.
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Top(80);

// Setzen Sie die Höhe der Form, wodurch die Breite automatisch skaliert wird, um die Abmessungen beizubehalten.
shape->set_Height(125);

ASPOSE_ASSERT_EQ(125.0, shape->get_Width());

// Die Eigenschaften "Bottom" und "Right" enthalten die unteren und rechten Kanten des Bildes.
ASPOSE_ASSERT_EQ(shape->get_Top() + shape->get_Height(), shape->get_Bottom());
ASPOSE_ASSERT_EQ(shape->get_Left() + shape->get_Width(), shape->get_Right());

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPositionSize.docx");
```


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

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
