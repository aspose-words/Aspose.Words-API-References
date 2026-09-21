---
title: "Aspose::Words::Drawing::ShapeBase::get_ZOrder metod"
linktitle: "get_ZOrder"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_ZOrder metod. Bestämmer visningsordningen för överlappande former i C++."
type: docs
weight: 57000
url: /sv/cpp/aspose.words.drawing/shapebase/get_zorder/
---
## ShapeBase::get_ZOrder method


Bestämmer visningsordningen för överlappande former.

```cpp
int32_t Aspose::Words::Drawing::ShapeBase::get_ZOrder()
```

## Anmärkningar


Har endast effekt för former på toppnivå.

Standardvärdet är 0.

Numret representerar staplingsprioriteten. En form med ett högre nummer kommer att visas som om den överlappade ("framför") en form med ett lägre nummer.

Ordningen för överlappande former är oberoende för former i sidhuvudet och i dokumentets huvudtext.

Visningsordningen för underformer i en gruppform bestäms av deras ordning inom gruppformen.

## Exempel



Visar hur man manipulerar ordningen på former.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga tre rektanglar med olika färger som delvis överlappar varandra.
// När vi infogar en form som överlappar en annan form placerar Aspose.Words den nyare formen ovanpå den äldre.
// Den ljusgröna rektangeln kommer att överlappa den ljusblå rektangeln och delvis dölja den,
// och den ljusblå rektangeln kommer att dölja den orangea rektangeln.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_Orange());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 150, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 150, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 200, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 200, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_LightGreen());

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

// Egenskapen "ZOrder" för en form bestämmer dess staplingsprioritet bland andra överlappande former.
// Om två överlappande former har olika "ZOrder"-värden,
// Microsoft Word placerar formen med ett högre värde ovanpå formen med det lägre värdet.
// Ställ in "ZOrder"-värdena för våra former för att placera den första orangea rektangeln ovanpå den andra ljusblå.
// och den andra ljusblå rektangeln ovanpå den tredje ljusgröna rektangeln.
// Detta kommer att vända deras ursprungliga staplingsordning.
shapes[0]->set_ZOrder(3);
shapes[1]->set_ZOrder(2);
shapes[2]->set_ZOrder(1);

doc->Save(get_ArtifactsDir() + u"Shape.ZOrder.docx");
```

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
