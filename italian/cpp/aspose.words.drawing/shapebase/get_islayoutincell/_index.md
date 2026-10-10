---
title: "Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell metodo"
linktitle: "get_IsLayoutInCell"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell metodo. Ottiene o imposta un flag che indica se la forma è visualizzata all'interno di una tabella o al di fuori di essa in C++."
type: docs
weight: 32000
url: /it/cpp/aspose.words.drawing/shapebase/get_islayoutincell/
---
## ShapeBase::get_IsLayoutInCell method


Ottiene o imposta un flag che indica se la forma è visualizzata all'interno di una tabella o al di fuori di essa.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell()
```

## Note


Il valore predefinito è **true**.

Ha effetto solo per le forme di livello superiore, la proprietà [WrapType](../get_wraptype/) della quale è impostata a un valore diverso da [Inline](../../../aspose.words/inline/).

## Esempi



Mostra come determinare come visualizzare una forma in una cella di tabella.
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

// Imposta la proprietà "IsLayoutInCell" su "true" per visualizzare la forma come elemento inline all'interno del paragrafo della cella.
// L'origine delle coordinate che determinerà la posizione della forma sarà l'angolo in alto a sinistra della cella della forma.
// Se ridimensioniamo la cella, la forma si sposterà per mantenere la stessa posizione a partire dall'angolo in alto a sinistra della cella.
// Imposta la proprietà "IsLayoutInCell" su "false" per visualizzare la forma come una forma fluttuante indipendente.
// L'origine delle coordinate che determinerà la posizione della forma sarà l'angolo in alto a sinistra della pagina,
// e la forma non risponderà a nessun ridimensionamento della sua cella.
shape->set_IsLayoutInCell(isLayoutInCell);

// Possiamo applicare la proprietà "IsLayoutInCell" solo alle forme fluttuanti.
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

doc->Save(get_ArtifactsDir() + u"Shape.LayoutInTableCell.docx");
```

## Vedi anche

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
