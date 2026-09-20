---
title: "Aspose::Words::Drawing::ShapeBase::get_BoundsInPoints método"
linktitle: "get_BoundsInPoints"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShapeBase::get_BoundsInPoints método. Obtiene la ubicación y el tamaño del bloque contenedor de la forma en puntos, relativo al ancla de la forma superior en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.drawing/shapebase/get_boundsinpoints/
---
## ShapeBase::get_BoundsInPoints method


Obtiene la ubicación y el tamaño del bloque contenedor de la forma en puntos, relativo al ancla de la forma más alta.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::get_BoundsInPoints()
```


## Ejemplos



Muestra cómo verificar los límites del bloque contenedor de la forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Line, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 50, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 50, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->set_StrokeColor(System::Drawing::Color::get_Orange());

// Aunque la línea en sí ocupa poco espacio en la página del documento,
// ocupa un bloque contenedor rectangular, cuyo tamaño podemos determinar usando las propiedades "Bounds".
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(50.0f, 50.0f, 100.0f, 100.0f), shape->get_Bounds());
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(50.0f, 50.0f, 100.0f, 100.0f), shape->get_BoundsInPoints());

// Cree una forma de grupo y luego establezca el tamaño de su bloque contenedor usando la propiedad "Bounds".
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f));

ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f), group->get_BoundsInPoints());

// Cree un rectángulo, verifique el tamaño de su bloque delimitador y luego agréguelo a la forma de grupo.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(700);
shape->set_Top(700);

ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(700.0f, 700.0f, 100.0f, 100.0f), shape->get_BoundsInPoints());

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// El plano de coordenadas de la forma de grupo tiene su origen en la esquina superior izquierda de su bloque contenedor,
// y las coordenadas x e y de (1000, 1000) en la esquina inferior derecha.
// Nuestra forma de grupo mide 250x250pt, por lo que cada 4pt en el plano de coordenadas de la forma de grupo
// se traduce a 1pt en el plano de coordenadas del cuerpo del documento.
// Cada forma que insertamos también se reducirá de tamaño en un factor de 4.
// El cambio en la propiedad "BoundsInPoints" de la forma reflejará esto.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(175.0f, 275.0f, 25.0f, 25.0f), shape->get_BoundsInPoints());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::GroupShape>>(group);

// Inserte una forma y colóquela fuera de los límites del bloque contenedor de la forma de grupo.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(1000);
shape->set_Top(1000);

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// La huella de la forma de grupo en el cuerpo del documento ha aumentado, pero el bloque contenedor sigue siendo el mismo.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f), group->get_BoundsInPoints());
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(250.0f, 350.0f, 25.0f, 25.0f), shape->get_BoundsInPoints());

doc->Save(get_ArtifactsDir() + u"Shape.Bounds.docx");
```

## Ver también

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
