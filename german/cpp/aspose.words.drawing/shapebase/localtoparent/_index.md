---
title: "Aspose::Words::Drawing::ShapeBase::LocalToParent Methode"
linktitle: "LocalToParent"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::LocalToParent Methode. Konvertiert einen Wert vom lokalen Koordinatenraum in den Koordinatenraum der übergeordneten Form in C++."
type: docs
weight: 61000
url: /de/cpp/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase::LocalToParent method


Konvertiert einen Wert vom lokalen Koordinatenraum in den Koordinatenraum der übergeordneten Form.

```cpp
System::Drawing::PointF Aspose::Words::Drawing::ShapeBase::LocalToParent(System::Drawing::PointF value)
```


## Beispiele



Zeigt, wie man die x- und y-Koordinatenposition auf der Koordinatenebene einer Form in eine Position auf der Koordinatenebene der übergeordneten Form übersetzt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Fügen Sie eine Gruppierung ein und platzieren Sie sie 100 Punkte unterhalb und rechts von
// dem x- und Y-Koordinatenursprung des Dokuments.
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(100.0f, 100.0f, 500.0f, 500.0f));

// Verwenden Sie die Methode "LocalToParent", um zu bestimmen, dass (0, 0) in den internen x- und y-Koordinaten der Gruppe
// auf (100, 100) des Koordinatensystems der übergeordneten Form liegt. Der Elternteil der Gruppierung ist das Dokument selbst.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(100.0f, 100.0f), group->LocalToParent(System::Drawing::PointF(0.0f, 0.0f)));

// Standardmäßig hat die interne Koordinatenebene einer Form die obere linke Ecke bei (0, 0),
// und die untere rechte Ecke bei (1000, 1000). Aufgrund ihrer Größe deckt unsere Gruppierung einen Bereich von 500pt x 500pt ab
// in der Dokumentenebene ab. Das bedeutet, dass eine Bewegung von 1pt in der Koordinatenebene des Dokuments übersetzt wird
// zu einer Bewegung von 2pt in der Koordinatenebene der Gruppierung.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(150.0f, 150.0f), group->LocalToParent(System::Drawing::PointF(100.0f, 100.0f)));
ASPOSE_ASSERT_EQ(System::Drawing::PointF(200.0f, 200.0f), group->LocalToParent(System::Drawing::PointF(200.0f, 200.0f)));
ASPOSE_ASSERT_EQ(System::Drawing::PointF(250.0f, 250.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Verschieben Sie den Ursprung der x- und y-Achse der Gruppierung von der oberen linken Ecke zur Mitte.
// Damit werden die internen Koordinaten der Gruppe relativ zu den Dokumentkoordinaten noch weiter verschoben.
group->set_CoordOrigin(System::Drawing::Point(-250, -250));

ASPOSE_ASSERT_EQ(System::Drawing::PointF(375.0f, 375.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Das Ändern der Skalierung der Koordinatenebene wirkt sich ebenfalls auf relative Positionen aus.
group->set_CoordSize(System::Drawing::Size(500, 500));

ASPOSE_ASSERT_EQ(System::Drawing::PointF(650.0f, 650.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Wenn wir einer Gruppe eine Form hinzufügen möchten, wobei wir ihre Position anhand einer Position im Dokument festlegen,
// müssen wir zunächst einen Ort in der Gruppierung bestimmen, der mit der Position im Dokument übereinstimmt.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(700.0f, 700.0f), group->LocalToParent(System::Drawing::PointF(350.0f, 350.0f)));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(700);
shape->set_Top(700);

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::GroupShape>>(group);

doc->Save(get_ArtifactsDir() + u"Shape.LocalToParent.docx");
```

## Siehe auch

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
