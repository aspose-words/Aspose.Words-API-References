---
title: "Aspose::Words::Drawing::ShapeBase::get_DistanceBottom Methode"
linktitle: "get_DistanceBottom"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_DistanceBottom Methode. Gibt den Abstand (in Punkten) zwischen dem Dokumenttext und dem unteren Rand der Form zurück oder setzt ihn in C++."
type: docs
weight: 15000
url: /de/cpp/aspose.words.drawing/shapebase/get_distancebottom/
---
## ShapeBase::get_DistanceBottom method


Liest oder setzt den Abstand (in Punkten) zwischen dem Dokumenttext und der unteren Kante der Form.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_DistanceBottom()
```

## Hinweise


Der Standardwert ist 0.

Wirkt nur bei Formen der obersten Ebene.

## Beispiele



Zeigt, wie der Umbruchabstand für einen Text, der eine Form umgibt, festgelegt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie ein Rechteck ein und lassen Sie den Text eng um seine Begrenzungen fließen.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 150, 150);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Tight);

// Setzen Sie den Mindestabstand zwischen der Form und dem umgebenden Text auf 40 pt von allen Seiten.
shape->set_DistanceTop(40);
shape->set_DistanceBottom(40);
shape->set_DistanceLeft(40);
shape->set_DistanceRight(40);

// Verschieben Sie die Form näher zur Seitenmitte und drehen Sie sie anschließend um 60 Grad im Uhrzeigersinn.
shape->set_Top(75);
shape->set_Left(150);
shape->set_Rotation(60);

// Fügen Sie Text hinzu, der um die Form fließt.
builder->get_Font()->set_Size(24);
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc->Save(get_ArtifactsDir() + u"Shape.Coordinates.docx");
```

## Siehe auch

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
