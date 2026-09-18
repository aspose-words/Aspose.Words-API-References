---
title: "Aspose::Words::Drawing::ShapeBase::get_Bounds Methode"
linktitle: "get_Bounds"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_Bounds Methode. Liest oder setzt die Position und Größe des enthaltenden Blocks der Form in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words.drawing/shapebase/get_bounds/
---
## ShapeBase::get_Bounds method


Liest oder setzt den Ort und die Größe des umgebenden Blocks der Form.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::get_Bounds()
```

## Hinweise


Ignoriert die Sperrung des Seitenverhältnisses beim Setzen.

Für eine Form auf oberster Ebene ist der Wert in Punkten und relativ zum Anker der Form.

Für Formen in einer Gruppe ist der Wert im Koordinatenraum und in den Einheiten der übergeordneten Gruppe.

## Beispiele



Zeigt, wie man eine Gruppenform erstellt und befüllt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Erstellen Sie eine Gruppenform. Eine Gruppenform kann eine Sammlung von untergeordneten Formknoten anzeigen.
// In Microsoft Word führt ein Klick innerhalb der Begrenzung der Gruppenform oder auf einer der untergeordneten Formen der Gruppenform dazu,
// alle anderen untergeordneten Formen innerhalb dieser Gruppe auszuwählen und ermöglicht es uns, alle Formen gleichzeitig zu skalieren und zu verschieben.
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);

ASSERT_EQ(Aspose::Words::Drawing::WrapType::None, group->get_WrapType());

// Erstellen Sie eine 400pt x 400pt Gruppenform und platzieren Sie sie am Koordinatenursprung der schwebenden Formen des Dokuments.
group->set_Bounds(System::Drawing::RectangleF(0.0f, 0.0f, 400.0f, 400.0f));

// Setzen Sie die interne Koordinatenebene der Gruppe auf 500 x 500pt.
// Die obere linke Ecke der Gruppe hat die x- und y-Koordinate (0, 0),
// und die untere rechte Ecke hat die x- und y-Koordinate (500, 500).
group->set_CoordSize(System::Drawing::Size(500, 500));

// Setzen Sie die Koordinaten der oberen linken Ecke der Gruppe auf (-250, -250).
// Das Zentrum der Gruppe hat jetzt die x- und y-Koordinate (0, 0),
// und die untere rechte Ecke befindet sich bei (250, 250).
group->set_CoordOrigin(System::Drawing::Point(-250, -250));

// Erstellen Sie ein Rechteck, das die Begrenzung dieser Gruppierung anzeigt, und fügen Sie es der Gruppe hinzu.
auto child1 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
child1->set_Width(group->get_CoordSize().get_Width());
child1->set_Height(group->get_CoordSize().get_Height());
child1->set_Left(group->get_CoordOrigin().get_X());
child1->set_Top(group->get_CoordOrigin().get_Y());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child1);

// Sobald eine Form Teil einer Gruppierung ist, können wir auf sie als Kindknoten zugreifen und sie dann ändern.
(System::ExplicitCast<Aspose::Words::Drawing::Shape>(group->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Stroke()->set_DashStyle(Aspose::Words::Drawing::DashStyle::Dash);

// Erstellen Sie einen kleinen roten Stern und fügen Sie ihn in die Gruppe ein.
// Richten Sie die Form an dem Koordinatenursprung der Gruppe aus, den wir in die Mitte verschoben haben.
auto child2 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Star);
child2->set_Width(20);
child2->set_Height(20);
child2->set_Left(-10);
child2->set_Top(-10);
child2->set_FillColor(System::Drawing::Color::get_Red());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child2);

// Fügen Sie ein Rechteck ein und dann ein etwas kleineres Rechteck an derselben Stelle mit einem Bild ein.
// Neuere Formen, die wir zur Gruppe hinzufügen, überlappen ältere Formen. Das hellblaue Rechteck wird den roten Stern teilweise überlappen,
// und dann wird die Form mit dem Bild das hellblaue Rechteck überlappen und es als Rahmen verwenden.
// Wir können die "ZOrder"-Eigenschaften von Formen nicht verwenden, um ihre Anordnung innerhalb einer Gruppierung zu manipulieren.
auto child3 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
child3->set_Width(250);
child3->set_Height(250);
child3->set_Left(-250);
child3->set_Top(-250);
child3->set_FillColor(System::Drawing::Color::get_LightBlue());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child3);

auto child4 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
child4->set_Width(200);
child4->set_Height(200);
child4->set_Left(-225);
child4->set_Top(-225);
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child4);

(System::ExplicitCast<Aspose::Words::Drawing::Shape>(group->GetChild(Aspose::Words::NodeType::Shape, 3, true)))->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Fügen Sie ein Textfeld in die Gruppierung ein. Setzen Sie die "Left"-Eigenschaft, sodass die rechte Kante des Textfelds
// die rechte Begrenzung der Gruppierung berührt. Setzen Sie die "Top"-Eigenschaft, sodass das Textfeld außerhalb
// der Begrenzung der Gruppierung liegt, wobei seine obere Kante entlang der unteren Randlinie der Gruppierung ausgerichtet ist.
auto child5 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
child5->set_Width(200);
child5->set_Height(50);
child5->set_Left(group->get_CoordSize().get_Width() + group->get_CoordOrigin().get_X() - 200);
child5->set_Top(group->get_CoordSize().get_Height() + group->get_CoordOrigin().get_Y());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child5);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(group);
builder->MoveTo((System::ExplicitCast<Aspose::Words::Drawing::Shape>(group->GetChild(Aspose::Words::NodeType::Shape, 4, true)))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"Shape.GroupShape.docx");
```


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
