---
title: "Aspose::Words::Drawing::ShapeBase::LocalToParent método"
linktitle: "LocalToParent"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShapeBase::LocalToParent método. Convierte un valor del espacio de coordenadas local al espacio de coordenadas de la forma padre en C++."
type: docs
weight: 61000
url: /es/cpp/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase::LocalToParent method


Convierte un valor del espacio de coordenadas local al espacio de coordenadas de la forma padre.

```cpp
System::Drawing::PointF Aspose::Words::Drawing::ShapeBase::LocalToParent(System::Drawing::PointF value)
```


## Ejemplos



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
