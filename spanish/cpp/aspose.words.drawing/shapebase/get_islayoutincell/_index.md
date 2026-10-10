---
title: "Método Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell"
linktitle: "get_IsLayoutInCell"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell. Obtiene o establece una bandera que indica si la forma se muestra dentro de una tabla o fuera de ella en C++."
type: docs
weight: 32000
url: /es/cpp/aspose.words.drawing/shapebase/get_islayoutincell/
---
## ShapeBase::get_IsLayoutInCell method


Obtiene o establece una bandera que indica si la forma se muestra dentro de una tabla o fuera de ella.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell()
```

## Observaciones


El valor predeterminado es **true**.

Tiene efecto solo para formas de nivel superior, la propiedad [WrapType](../get_wraptype/) de la cual está establecida a un valor distinto de [Inline](../../../aspose.words/inline/).

## Ejemplos



Muestra cómo determinar cómo mostrar una forma en una celda de tabla.
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

// Establezca la propiedad "IsLayoutInCell" a "true" para mostrar la forma como un elemento en línea dentro del párrafo de la celda.
// El origen de coordenadas que determinará la ubicación de la forma será la esquina superior izquierda de la celda de la forma.
// Si redimensionamos la celda, la forma se moverá para mantener la misma posición partiendo de la esquina superior izquierda de la celda.
// Establezca la propiedad "IsLayoutInCell" a "false" para mostrar la forma como una forma flotante independiente.
// El origen de coordenadas que determinará la ubicación de la forma será la esquina superior izquierda de la página,
// y la forma no responderá a ningún redimensionamiento de su celda.
shape->set_IsLayoutInCell(isLayoutInCell);

// Solo podemos aplicar la propiedad "IsLayoutInCell" a formas flotantes.
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

doc->Save(get_ArtifactsDir() + u"Shape.LayoutInTableCell.docx");
```

## Ver también

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
