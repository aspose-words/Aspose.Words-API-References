---
title: "Aspose::Words::Drawing::ShapeBase::get_DistanceBottom‑metod"
linktitle: "get_DistanceBottom"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_DistanceBottom‑metod. Returnerar eller anger avståndet (i punkter) mellan dokumenttexten och formens nedre kant i C++."
type: docs
weight: 15000
url: /sv/cpp/aspose.words.drawing/shapebase/get_distancebottom/
---
## ShapeBase::get_DistanceBottom method


Returnerar eller anger avståndet (i punkter) mellan dokumenttexten och formens nedre kant.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_DistanceBottom()
```

## Anmärkningar


Standardvärdet är 0.

Har endast effekt för former på toppnivå.

## Exempel



Visar hur man ställer in omslagsavståndet för text som omger en form.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en rektangel och låt texten omsluta den tätt runt dess gränser.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 150, 150);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Tight);

// Ställ in det minsta avståndet mellan formen och omgivande text till 40pt från alla sidor.
shape->set_DistanceTop(40);
shape->set_DistanceBottom(40);
shape->set_DistanceLeft(40);
shape->set_DistanceRight(40);

// Flytta formen närmare sidans centrum och rotera sedan formen 60 grader medurs.
shape->set_Top(75);
shape->set_Left(150);
shape->set_Rotation(60);

// Lägg till text som kommer att flöda runt formen.
builder->get_Font()->set_Size(24);
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc->Save(get_ArtifactsDir() + u"Shape.Coordinates.docx");
```

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
