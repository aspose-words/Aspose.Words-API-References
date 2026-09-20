---
title: "Método Aspose::Words::Drawing::ShapeBase::get_CoordOrigin"
linktitle: "get_CoordOrigin"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::ShapeBase::get_CoordOrigin. Las coordenadas en la esquina superior izquierda del bloque contenedor de esta forma en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words.drawing/shapebase/get_coordorigin/
---
## ShapeBase::get_CoordOrigin method


Las coordenadas en la esquina superior izquierda del bloque contenedor de esta forma.

```cpp
System::Drawing::Point Aspose::Words::Drawing::ShapeBase::get_CoordOrigin()
```

## Observaciones


El valor predeterminado es (0,0).

## Ejemplos



Muestra cómo crear y rellenar una forma grupal.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Cree una forma grupal. Una forma grupal puede mostrar una colección de nodos de forma hijos.
// En Microsoft Word, al hacer clic dentro del contorno de la forma grupal o en una de las formas hijas de la forma grupal, se
// seleccionarán todas las demás formas hijas dentro de este grupo y nos permitirán escalar y mover todas las formas a la vez.
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);

ASSERT_EQ(Aspose::Words::Drawing::WrapType::None, group->get_WrapType());

// Cree una forma grupal de 400pt x 400pt y colóquela en el origen de coordenadas de la forma flotante del documento.
group->set_Bounds(System::Drawing::RectangleF(0.0f, 0.0f, 400.0f, 400.0f));

// Establezca el tamaño del plano de coordenadas interno del grupo a 500 x 500pt.
// La esquina superior izquierda del grupo tendrá una coordenada x e y de (0, 0),
// y la esquina inferior derecha tendrá una coordenada x e y de (500, 500).
group->set_CoordSize(System::Drawing::Size(500, 500));

// Establezca las coordenadas de la esquina superior izquierda del grupo en (-250, -250).
// El centro del grupo ahora tendrá un valor de coordenada x e y de (0, 0),
// y la esquina inferior derecha estará en (250, 250).
group->set_CoordOrigin(System::Drawing::Point(-250, -250));

// Cree un rectángulo que mostrará el contorno de esta forma de grupo y agréguelo al grupo.
auto child1 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
child1->set_Width(group->get_CoordSize().get_Width());
child1->set_Height(group->get_CoordSize().get_Height());
child1->set_Left(group->get_CoordOrigin().get_X());
child1->set_Top(group->get_CoordOrigin().get_Y());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child1);

// Una vez que una forma es parte de una forma de grupo, podemos acceder a ella como un nodo hijo y luego modificarla.
(System::ExplicitCast<Aspose::Words::Drawing::Shape>(group->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Stroke()->set_DashStyle(Aspose::Words::Drawing::DashStyle::Dash);

// Cree una pequeña estrella roja e insértela en el grupo.
// Alinee la forma con el origen de coordenadas del grupo, que hemos movido al centro.
auto child2 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Star);
child2->set_Width(20);
child2->set_Height(20);
child2->set_Left(-10);
child2->set_Top(-10);
child2->set_FillColor(System::Drawing::Color::get_Red());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child2);

// Inserte un rectángulo y luego inserte un rectángulo ligeramente más pequeño en el mismo lugar con una imagen.
// Las formas más recientes que añadimos al grupo se superponen a las formas más antiguas. El rectángulo azul claro se superpondrá parcialmente a la estrella roja,
// y luego la forma con la imagen se superpondrá al rectángulo azul claro, usándolo como marco.
// No podemos usar las propiedades "ZOrder" de las formas para manipular su disposición dentro de una forma de grupo.
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

// Inserte un cuadro de texto en la forma de grupo. Establezca la propiedad "Left" para que el borde derecho del cuadro de texto
// toque el límite derecho de la forma de grupo. Establezca la propiedad "Top" para que el cuadro de texto quede fuera
// del límite de la forma de grupo, con su parte superior alineada a lo largo del margen inferior de la forma de grupo.
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


Muestra cómo traducir la ubicación de coordenadas x e y en el plano de coordenadas de una forma a una ubicación en el plano de coordenadas de la forma padre.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Inserte una forma de grupo y colóquela 100 puntos abajo y a la derecha de
// el punto de origen de coordenadas x y Y del documento.
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(100.0f, 100.0f, 500.0f, 500.0f));

// Utilice el método "LocalToParent" para determinar que (0, 0) en las coordenadas internas x e y del grupo
// se encuentra en (100, 100) del sistema de coordenadas de su forma padre. El padre de la forma de grupo es el propio documento.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(100.0f, 100.0f), group->LocalToParent(System::Drawing::PointF(0.0f, 0.0f)));

// Por defecto, el plano de coordenadas interno de una forma tiene la esquina superior izquierda en (0, 0),
// y la esquina inferior derecha en (1000, 1000). Debido a su tamaño, nuestra forma de grupo cubre un área de 500pt x 500pt
// en el plano del documento. Esto significa que un movimiento de 1pt en el plano de coordenadas del documento se traducirá
// a un movimiento de 2pts en el plano de coordenadas de la forma de grupo.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(150.0f, 150.0f), group->LocalToParent(System::Drawing::PointF(100.0f, 100.0f)));
ASPOSE_ASSERT_EQ(System::Drawing::PointF(200.0f, 200.0f), group->LocalToParent(System::Drawing::PointF(200.0f, 200.0f)));
ASPOSE_ASSERT_EQ(System::Drawing::PointF(250.0f, 250.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Mueva el origen de los ejes x e y del grupo de formas desde la esquina superior izquierda al centro.
// Esto desplazará aún más las coordenadas internas del grupo en relación con las coordenadas del documento.
group->set_CoordOrigin(System::Drawing::Point(-250, -250));

ASPOSE_ASSERT_EQ(System::Drawing::PointF(375.0f, 375.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Cambiar la escala del plano de coordenadas también afectará las ubicaciones relativas.
group->set_CoordSize(System::Drawing::Size(500, 500));

ASPOSE_ASSERT_EQ(System::Drawing::PointF(650.0f, 650.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Si deseamos agregar una forma a este grupo mientras definimos su ubicación basándonos en una ubicación del documento,
// necesitaremos primero confirmar una ubicación en el grupo de formas que coincida con la ubicación del documento.
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

## Ver también

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
