---
title: "Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell method"
linktitle: "get_IsLayoutInCell"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell-Methode. Gibt ein Flag zurück oder setzt es, das angibt, ob die Form innerhalb einer Tabelle oder außerhalb davon in C++ angezeigt wird."
type: docs
weight: 32000
url: /de/cpp/aspose.words.drawing/shapebase/get_islayoutincell/
---
## ShapeBase::get_IsLayoutInCell method


Liest oder legt ein Flag fest, das angibt, ob die Form innerhalb einer Tabelle oder außerhalb davon angezeigt wird.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell()
```

## Hinweise


Der Standardwert ist **true**.

Wirkt nur bei Formen der obersten Ebene, deren Eigenschaft [WrapType](../get_wraptype/) auf einen anderen Wert als [Inline](../../../aspose.words/inline/) gesetzt ist.

## Beispiele



Zeigt, wie man bestimmt, wie eine Form in einer Tabellenzelle angezeigt wird.
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

// Setzen Sie die Eigenschaft "IsLayoutInCell" auf "true", um die Form als Inline-Element innerhalb des Absatzes der Zelle anzuzeigen.
// Der Koordinatenursprung, der den Standort der Form bestimmt, ist die obere linke Ecke der Zelle der Form.
// Wenn wir die Zelle neu skalieren, verschiebt sich die Form, um die gleiche Position ab der oberen linken Ecke der Zelle beizubehalten.
// Setzen Sie die Eigenschaft "IsLayoutInCell" auf "false", um die Form als unabhängige schwebende Form anzuzeigen.
// Der Koordinatenursprung, der den Standort der Form bestimmt, ist die obere linke Ecke der Seite,
// und die Form reagiert nicht auf eine Größenänderung ihrer Zelle.
shape->set_IsLayoutInCell(isLayoutInCell);

// Wir können die Eigenschaft "IsLayoutInCell" nur auf schwebende Formen anwenden.
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

doc->Save(get_ArtifactsDir() + u"Shape.LayoutInTableCell.docx");
```

## Siehe auch

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
