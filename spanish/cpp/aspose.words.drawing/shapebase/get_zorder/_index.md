---
title: "Método Aspose::Words::Drawing::ShapeBase::get_ZOrder"
linktitle: "get_ZOrder"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::ShapeBase::get_ZOrder. Determina el orden de visualización de formas superpuestas en C++."
type: docs
weight: 57000
url: /es/cpp/aspose.words.drawing/shapebase/get_zorder/
---
## ShapeBase::get_ZOrder method


Determina el orden de visualización de las formas superpuestas.

```cpp
int32_t Aspose::Words::Drawing::ShapeBase::get_ZOrder()
```

## Observaciones


Tiene efecto solo para formas de nivel superior.

El valor predeterminado es 0.

El número representa la precedencia de apilamiento. Una forma con un número mayor se mostrará como si estuviera superpuesta ("delante" de) una forma con un número menor.

El orden de las formas superpuestas es independiente para las formas en el encabezado y en el texto principal del documento.

El orden de visualización de las formas hijas en una forma de grupo se determina por su orden dentro de la forma de grupo.

## Ejemplos



Muestra cómo manipular el orden de las formas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte tres rectángulos de colores diferentes que se superpongan parcialmente entre sí.
// Cuando insertamos una forma que se superpone a otra forma, Aspose.Words coloca la forma más nueva encima de la anterior.
// El rectángulo verde claro se superpondrá al rectángulo azul claro y lo oscurecerá parcialmente,
// y el rectángulo azul claro oscurecerá el rectángulo naranja.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_Orange());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 150, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 150, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 200, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 200, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_LightGreen());

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

// La propiedad "ZOrder" de una forma determina su prioridad de apilamiento entre otras formas superpuestas.
// Si dos formas superpuestas tienen valores diferentes de "ZOrder",
// Microsoft Word colocará la forma con un valor mayor sobre la forma con el valor menor.
// Establezca los valores de "ZOrder" de nuestras formas para colocar el primer rectángulo naranja sobre el segundo rectángulo azul claro
// y el segundo rectángulo azul claro sobre el tercer rectángulo verde claro.
// Esto invertirá su orden de apilamiento original.
shapes[0]->set_ZOrder(3);
shapes[1]->set_ZOrder(2);
shapes[2]->set_ZOrder(1);

doc->Save(get_ArtifactsDir() + u"Shape.ZOrder.docx");
```

## Ver también

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
