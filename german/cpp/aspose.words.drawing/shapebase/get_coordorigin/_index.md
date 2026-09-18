---
title: "Aspose::Words::Drawing::ShapeBase::get_CoordOrigin-Methode"
linktitle: "get_CoordOrigin"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_CoordOrigin-Methode. Die Koordinaten an der oberen linken Ecke des enthaltenden Blocks dieser Form in C++."
type: docs
weight: 13000
url: /de/cpp/aspose.words.drawing/shapebase/get_coordorigin/
---
## ShapeBase::get_CoordOrigin method


Die Koordinaten in der oberen linken Ecke des umgebenden Blocks dieser Form.

```cpp
System::Drawing::Point Aspose::Words::Drawing::ShapeBase::get_CoordOrigin()
```

## Hinweise


Der Standardwert ist (0,0).

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
