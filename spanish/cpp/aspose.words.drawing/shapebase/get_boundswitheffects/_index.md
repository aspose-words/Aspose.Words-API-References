---
title: "Aspose::Words::Drawing::ShapeBase::get_BoundsWithEffects método"
linktitle: "get_BoundsWithEffects"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShapeBase::get_BoundsWithEffects método. Obtiene la extensión final que tiene este objeto de forma después de aplicar los efectos de dibujo. El valor se mide en puntos en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words.drawing/shapebase/get_boundswitheffects/
---
## ShapeBase::get_BoundsWithEffects method


Obtiene la extensión final que tiene este objeto forma después de aplicar efectos de dibujo. El valor se mide en puntos.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::get_BoundsWithEffects()
```


## Ejemplos



Muestra cómo comprobar cómo los límites de una forma se ven afectados por los efectos de forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape shadow effect.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

// Las dos formas son idénticas en cuanto a dimensiones y tipo de forma.
ASPOSE_ASSERT_EQ(shapes[0]->get_Width(), shapes[1]->get_Width());
ASPOSE_ASSERT_EQ(shapes[0]->get_Height(), shapes[1]->get_Height());
ASSERT_EQ(shapes[0]->get_ShapeType(), shapes[1]->get_ShapeType());

// La primera forma no tiene efectos, y la segunda tiene una sombra y un contorno grueso.
// Estos efectos hacen que el tamaño de la silueta de la segunda forma sea mayor que el de la primera.
// Aunque el tamaño del rectángulo se muestra al hacer clic en estas formas en Microsoft Word,
// los límites exteriores visibles de la segunda forma están afectados por la sombra y el contorno y, por lo tanto, son más grandes.
// Podemos usar el método "AdjustWithEffects" para ver el tamaño real de la forma.
ASPOSE_ASSERT_EQ(0.0, shapes[0]->get_StrokeWeight());
ASPOSE_ASSERT_EQ(20.0, shapes[1]->get_StrokeWeight());
ASSERT_FALSE(shapes[0]->get_ShadowEnabled());
ASSERT_TRUE(shapes[1]->get_ShadowEnabled());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = shapes[0];

// Cree un objeto RectangleF, que representa un rectángulo,
// que podríamos usar potencialmente como las coordenadas y límites de una forma.
System::Drawing::RectangleF rectangleF(200.0f, 200.0f, 1000.0f, 1000.0f);

// Ejecute este método para obtener el tamaño del rectángulo ajustado por todos nuestros efectos de forma.
System::Drawing::RectangleF rectangleFOut = shape->AdjustWithEffects(rectangleF);

// Dado que la forma no tiene efectos que cambien el borde, sus dimensiones de límite no se ven afectadas.
ASPOSE_ASSERT_EQ(200, rectangleFOut.get_X());
ASPOSE_ASSERT_EQ(200, rectangleFOut.get_Y());
ASPOSE_ASSERT_EQ(1000, rectangleFOut.get_Width());
ASPOSE_ASSERT_EQ(1000, rectangleFOut.get_Height());

// Verifique la extensión final de la primera forma, en puntos.
ASPOSE_ASSERT_EQ(0, shape->get_BoundsWithEffects().get_X());
ASPOSE_ASSERT_EQ(0, shape->get_BoundsWithEffects().get_Y());
ASPOSE_ASSERT_EQ(147, shape->get_BoundsWithEffects().get_Width());
ASPOSE_ASSERT_EQ(147, shape->get_BoundsWithEffects().get_Height());

shape = shapes[1];
rectangleF = System::Drawing::RectangleF(200.0f, 200.0f, 1000.0f, 1000.0f);
rectangleFOut = shape->AdjustWithEffects(rectangleF);

// Los efectos de la forma han desplazado ligeramente la esquina superior izquierda aparente de la forma.
ASPOSE_ASSERT_EQ(171.5, rectangleFOut.get_X());
ASPOSE_ASSERT_EQ(167, rectangleFOut.get_Y());

// Los efectos también han afectado las dimensiones visibles de la forma.
ASPOSE_ASSERT_EQ(1045, rectangleFOut.get_Width());
ASPOSE_ASSERT_EQ(1133.5, rectangleFOut.get_Height());

// Los efectos también han afectado los límites visibles de la forma.
ASPOSE_ASSERT_EQ(-28.5, shape->get_BoundsWithEffects().get_X());
ASPOSE_ASSERT_EQ(-33, shape->get_BoundsWithEffects().get_Y());
ASPOSE_ASSERT_EQ(192, shape->get_BoundsWithEffects().get_Width());
ASPOSE_ASSERT_EQ(280.5, shape->get_BoundsWithEffects().get_Height());
```

## Ver también

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
