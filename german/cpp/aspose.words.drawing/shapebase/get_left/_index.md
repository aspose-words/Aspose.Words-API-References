---
title: "Aspose::Words::Drawing::ShapeBase::get_Left Methode"
linktitle: "get_Left"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_Left Methode. Gibt die Position der linken Kante des enthaltenden Blocks der Form zurück oder setzt sie in C++."
type: docs
weight: 38000
url: /de/cpp/aspose.words.drawing/shapebase/get_left/
---
## ShapeBase::get_Left method


Liest oder legt die Position der linken Kante des enthaltenden Blocks der Form fest.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Left()
```

## Hinweise


Für eine Form auf oberster Ebene ist der Wert in Punkten und relativ zum Anker der Form.

Für Formen in einer Gruppe ist der Wert im Koordinatenraum und in den Einheiten der übergeordneten Gruppe.

Der Standardwert ist 0.

Hat nur für schwebende Formen Wirkung.

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

## Siehe auch

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
