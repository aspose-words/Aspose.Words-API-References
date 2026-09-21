---
title: "Aspose::Words::Drawing::ShapeBase::get_Bounds metod"
linktitle: "get_Bounds"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_Bounds metod. Hämtar eller anger platsen och storleken på den omgivande blocket för formen i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.drawing/shapebase/get_bounds/
---
## ShapeBase::get_Bounds method


Hämtar eller anger platsen och storleken på formens innehållande block.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::get_Bounds()
```

## Anmärkningar


Ignorerar låsning av bildförhållandet vid inställning.

För en toppnivåform är värdet i punkter och relativt till formens ankare.

För former i en grupp är värdet i koordinatrymden och enheterna för den överordnade gruppen.

## Exempel



Visar hur man skapar och fyller en gruppform.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Skapa en gruppform. En gruppform kan visa en samling av underordnade formnoder.
// I Microsoft Word kommer ett klick inom gruppformens gräns eller på en av gruppformens underordnade former att
// välja alla andra underordnade former inom denna grupp och låta oss skala och flytta alla former på en gång.
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);

ASSERT_EQ(Aspose::Words::Drawing::WrapType::None, group->get_WrapType());

// Skapa en 400pt x 400pt gruppform och placera den vid dokumentets flytande formkoordinatursprung.
group->set_Bounds(System::Drawing::RectangleF(0.0f, 0.0f, 400.0f, 400.0f));

// Ställ in gruppens interna koordinatplan till 500 x 500pt.
// Gruppens övre vänstra hörn kommer att ha x- och y-koordinater på (0, 0),
// och det nedre högra hörnet kommer att ha x- och y-koordinater på (500, 500).
group->set_CoordSize(System::Drawing::Size(500, 500));

// Ställ in koordinaterna för gruppens övre vänstra hörn till (-250, -250).
// Gruppens centrum kommer nu att ha ett x- och y-koordinatvärde på (0, 0),
// och det nedre högra hörnet kommer att vara på (250, 250).
group->set_CoordOrigin(System::Drawing::Point(-250, -250));

// Skapa en rektangel som visar gränsen för denna gruppform och lägg till den i gruppen.
auto child1 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
child1->set_Width(group->get_CoordSize().get_Width());
child1->set_Height(group->get_CoordSize().get_Height());
child1->set_Left(group->get_CoordOrigin().get_X());
child1->set_Top(group->get_CoordOrigin().get_Y());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child1);

// När en form är en del av en gruppform kan vi komma åt den som en underordnad nod och sedan modifiera den.
(System::ExplicitCast<Aspose::Words::Drawing::Shape>(group->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Stroke()->set_DashStyle(Aspose::Words::Drawing::DashStyle::Dash);

// Skapa en liten röd stjärna och infoga den i gruppen.
// Rikta in formen med gruppens koordinatursprung, som vi har flyttat till centrum.
auto child2 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Star);
child2->set_Width(20);
child2->set_Height(20);
child2->set_Left(-10);
child2->set_Top(-10);
child2->set_FillColor(System::Drawing::Color::get_Red());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child2);

// Infoga en rektangel, och sedan infoga en något mindre rektangel på samma plats med en bild.
// Nyare former som vi lägger till i gruppen överlappar äldre former. Den ljusblå rektangeln kommer delvis att överlappa den röda stjärnan,
// och sedan kommer formen med bilden att överlappa den ljusblå rektangeln, och använda den som en ram.
// Vi kan inte använda egenskaperna \"ZOrder\" för former för att manipulera deras placering inom en gruppform.
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

// Infoga en textruta i gruppformen. Ställ in egenskapen \"Left\" så att textrutans högra kant
// rör den högra gränsen av gruppformen. Ställ in egenskapen \"Top\" så att textrutan sitter utanför
// gränsen för gruppformen, med dess övre storlek inriktad längs gruppformens nedre marginal.
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


Visar hur man verifierar gränserna för formens omgivande block.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Line, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 50, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 50, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->set_StrokeColor(System::Drawing::Color::get_Orange());

// Även om raden själv tar upp lite utrymme på dokumentets sida,
// Den upptar ett rektangulärt omgivande block, vars storlek vi kan bestämma med hjälp av egenskaperna "Bounds".
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(50.0f, 50.0f, 100.0f, 100.0f), shape->get_Bounds());
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(50.0f, 50.0f, 100.0f, 100.0f), shape->get_BoundsInPoints());

// Skapa en gruppform och sätt sedan storleken på dess omgivande block med hjälp av egenskapen "Bounds".
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f));

ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f), group->get_BoundsInPoints());

// Skapa en rektangel, verifiera storleken på dess omgivande block och lägg sedan till den i gruppformen.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(700);
shape->set_Top(700);

ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(700.0f, 700.0f, 100.0f, 100.0f), shape->get_BoundsInPoints());

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Koordinatplanet för gruppformen har sitt ursprung i det övre vänstra hörnet av dess omgivande block,
// och x- och y-koordinaterna för (1000, 1000) på det nedre högra hörnet.
// Vår gruppform är 250x250pt i storlek, så varje 4pt på gruppformens koordinatplan.
// översätts till 1pt i dokumentkroppens koordinatplan.
// Varje form som vi infogar kommer också att krympa i storlek med en faktor på 4.
// Ändringen i formens "BoundsInPoints"-egenskap kommer att återspegla detta.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(175.0f, 275.0f, 25.0f, 25.0f), shape->get_BoundsInPoints());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::GroupShape>>(group);

// Infoga en form och placera den utanför gränserna för gruppformens innehållande block.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(1000);
shape->set_Top(1000);

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Gruppformens fotavtryck i dokumentkroppen har ökat, men det innehållande blocket förblir detsamma.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f), group->get_BoundsInPoints());
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(250.0f, 350.0f, 25.0f, 25.0f), shape->get_BoundsInPoints());

doc->Save(get_ArtifactsDir() + u"Shape.Bounds.docx");
```

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
