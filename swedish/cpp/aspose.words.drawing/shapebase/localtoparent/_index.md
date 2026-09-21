---
title: "Aspose::Words::Drawing::ShapeBase::LocalToParent‑metod"
linktitle: "LocalToParent"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::LocalToParent‑metod. Konverterar ett värde från det lokala koordinatrymdet till koordinatrymdet för föräldraformen i C++."
type: docs
weight: 61000
url: /sv/cpp/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase::LocalToParent method


Konverterar ett värde från det lokala koordinatsystemet till föräldraformens koordinatsystem.

```cpp
System::Drawing::PointF Aspose::Words::Drawing::ShapeBase::LocalToParent(System::Drawing::PointF value)
```


## Exempel



Visar hur man översätter x- och y-koordinatplatsen på en forms koordinatplan till en plats på föräldraformens koordinatplan.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Infoga en gruppform och placera den 100 punkter nedanför och till höger om
// dokumentets x- och Y-koordinatursprungspunkt.
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(100.0f, 100.0f, 500.0f, 500.0f));

// Använd metoden \"LocalToParent\" för att bestämma att (0, 0) på gruppens interna x- och y-koordinater
// ligger på (100, 100) i dess föräldraforms koordinatsystem. Gruppformens förälder är själva dokumentet.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(100.0f, 100.0f), group->LocalToParent(System::Drawing::PointF(0.0f, 0.0f)));

// Som standard har en forms interna koordinatplan det övre vänstra hörnet vid (0, 0),
// och det nedre högra hörnet vid (1000, 1000). På grund av dess storlek täcker vår gruppform ett område på 500pt x 500pt
// i dokumentets plan. Detta betyder att en rörelse på 1pt i dokumentets koordinatplan kommer att översättas
// till en rörelse på 2pt på gruppformens koordinatplan.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(150.0f, 150.0f), group->LocalToParent(System::Drawing::PointF(100.0f, 100.0f)));
ASPOSE_ASSERT_EQ(System::Drawing::PointF(200.0f, 200.0f), group->LocalToParent(System::Drawing::PointF(200.0f, 200.0f)));
ASPOSE_ASSERT_EQ(System::Drawing::PointF(250.0f, 250.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Flytta gruppformens x- och y-axelursprung från det övre vänstra hörnet till centrum.
// Detta kommer att förskjuta gruppens interna koordinater relativt dokumentets koordinater ännu mer.
group->set_CoordOrigin(System::Drawing::Point(-250, -250));

ASPOSE_ASSERT_EQ(System::Drawing::PointF(375.0f, 375.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Att ändra skalan på koordinatplanet kommer också att påverka relativa positioner.
group->set_CoordSize(System::Drawing::Size(500, 500));

ASPOSE_ASSERT_EQ(System::Drawing::PointF(650.0f, 650.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Om vi vill lägga till en form i den här gruppen samtidigt som vi definierar dess plats baserat på en plats i dokumentet,
// måste vi först bekräfta en plats i gruppformen som matchar dokumentets plats.
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

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
