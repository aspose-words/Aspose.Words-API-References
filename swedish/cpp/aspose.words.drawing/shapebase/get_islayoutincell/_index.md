---
title: "Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell metod"
linktitle: "get_IsLayoutInCell"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell metod. Hämtar eller anger en flagga som visar om formen visas inuti en tabell eller utanför den i C++."
type: docs
weight: 32000
url: /sv/cpp/aspose.words.drawing/shapebase/get_islayoutincell/
---
## ShapeBase::get_IsLayoutInCell method


Hämtar eller anger en flagga som indikerar om formen visas inuti en tabell eller utanför den.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell()
```

## Anmärkningar


Standardvärdet är **true**.

Har endast effekt för former på toppnivå, egenskapen [WrapType](../get_wraptype/) för vilken är satt till ett värde annat än [Inline](../../../aspose.words/inline/).

## Exempel



Visar hur man bestämmer hur en form ska visas i en tabellcell.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_BottomPadding(20);
tableStyle->set_LeftPadding(10);
tableStyle->set_RightPadding(10);
tableStyle->set_TopPadding(20);
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Single);

table->set_Style(tableStyle);

builder->MoveTo(table->get_FirstRow()->get_FirstCell()->get_FirstParagraph());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 50, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);

// Ställ in egenskapen \"IsLayoutInCell\" till \"true\" för att visa formen som ett inline-element i cellens stycke.
// Koordinatursprunget som bestämmer figurens placering kommer att vara cellens övre vänstra hörn.
// Om vi ändrar storlek på cellen kommer formen att flyttas för att behålla samma position med början från cellens övre vänstra hörn.
// Ställ in egenskapen "IsLayoutInCell" till "false" för att visa formen som en självständig flytande form.
// Koordinatursprunget som kommer att bestämma formens position kommer att vara sidans övre vänstra hörn,
// och formen kommer inte att svara på någon omstorlek av dess cell.
shape->set_IsLayoutInCell(isLayoutInCell);

// Vi kan endast tillämpa egenskapen "IsLayoutInCell" på flytande former.
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

doc->Save(get_ArtifactsDir() + u"Shape.LayoutInTableCell.docx");
```

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
