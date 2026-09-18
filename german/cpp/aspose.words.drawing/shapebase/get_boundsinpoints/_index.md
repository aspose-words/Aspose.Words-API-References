---
title: "Aspose::Words::Drawing::ShapeBase::get_BoundsInPoints Methode"
linktitle: "get_BoundsInPoints"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_BoundsInPoints Methode. Gibt die Position und Größe des umgebenden Blocks der Form in Punkten zurück, relativ zum Anker der obersten Form in C++."
type: docs
weight: 10000
url: /de/cpp/aspose.words.drawing/shapebase/get_boundsinpoints/
---
## ShapeBase::get_BoundsInPoints method


Liest den Ort und die Größe des umgebenden Blocks der Form in Punkten, relativ zum Anker der obersten Form.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::get_BoundsInPoints()
```


## Beispiele



Zeigt, wie man die Grenzen des Form-Containment-Blocks überprüft.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Line, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 50, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 50, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->set_StrokeColor(System::Drawing::Color::get_Orange());

// Obwohl die Zeile selbst nur wenig Platz auf der Dokumentseite einnimmt,
// belegt einen rechteckigen Containment-Block, dessen Größe wir mit den "Bounds"-Eigenschaften bestimmen können.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(50.0f, 50.0f, 100.0f, 100.0f), shape->get_Bounds());
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(50.0f, 50.0f, 100.0f, 100.0f), shape->get_BoundsInPoints());

// Erstellen Sie eine Gruppierung von Formen und setzen Sie anschließend die Größe ihres Containment-Blocks mithilfe der "Bounds"-Eigenschaft.
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f));

ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f), group->get_BoundsInPoints());

// Erstellen Sie ein Rechteck, überprüfen Sie die Größe seines Begrenzungsblocks und fügen Sie es anschließend zur Gruppierung von Formen hinzu.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(700);
shape->set_Top(700);

ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(700.0f, 700.0f, 100.0f, 100.0f), shape->get_BoundsInPoints());

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Das Koordinatensystem der Gruppierung von Formen hat seinen Ursprung in der oberen linken Ecke ihres Containment-Blocks,
// und die x‑ und y‑Koordinaten von (1000, 1000) in der unteren rechten Ecke.
// Unsere Gruppierung von Formen ist 250 × 250 pt groß, sodass jeder 4 pt auf dem Koordinatensystem der Gruppierung von Formen
// entspricht 1 pt im Koordinatensystem des Dokumentkörpers.
// Jede eingefügte Form wird ebenfalls um den Faktor 4 verkleinert.
// Die Änderung der "BoundsInPoints"‑Eigenschaft der Form wird dies widerspiegeln.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(175.0f, 275.0f, 25.0f, 25.0f), shape->get_BoundsInPoints());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::GroupShape>>(group);

// Fügen Sie eine Form ein und platzieren Sie sie außerhalb der Grenzen des Containment-Blocks der Gruppierung von Formen.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(1000);
shape->set_Top(1000);

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Der Fußabdruck der Gruppierung von Formen im Dokumentkörper hat zugenommen, aber der Containment-Block bleibt unverändert.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f), group->get_BoundsInPoints());
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(250.0f, 350.0f, 25.0f, 25.0f), shape->get_BoundsInPoints());

doc->Save(get_ArtifactsDir() + u"Shape.Bounds.docx");
```

## Siehe auch

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
