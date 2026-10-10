---
title: "Método Aspose::Words::Drawing::ShapeBase::get_Left"
linktitle: "get_Left"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::ShapeBase::get_Left. Obtiene o establece la posición del borde izquierdo del bloque contenedor de la forma en C++."
type: docs
weight: 38000
url: /es/cpp/aspose.words.drawing/shapebase/get_left/
---
## ShapeBase::get_Left method


Obtiene o establece la posición del borde izquierdo del bloque contenedor de la forma.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Left()
```

## Observaciones


Para una forma de nivel superior, el valor está en puntos y es relativo al ancla de la forma.

Para las formas en un grupo, el valor está en el espacio de coordenadas y unidades del grupo padre.

El valor predeterminado es 0.

Tiene efecto solo para formas flotantes.

## Ejemplos



Muestra cómo insertar una imagen flotante y especificar su posición y tamaño.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Configure la propiedad "RelativeHorizontalPosition" de la forma para tratar el valor de la propiedad "Left"
// como la distancia horizontal de la forma, en puntos, desde el lado izquierdo de la página.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);

// Establezca la distancia horizontal de la forma desde el lado izquierdo de la página a 100.
shape->set_Left(100);

// Utilice la propiedad "RelativeVerticalPosition" de manera similar para posicionar la forma 80 pt por debajo de la parte superior de la página.
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Top(80);

// Establezca la altura de la forma, lo que escalará automáticamente el ancho para preservar las dimensiones.
shape->set_Height(125);

ASPOSE_ASSERT_EQ(125.0, shape->get_Width());

// Las propiedades "Bottom" y "Right" contienen los bordes inferior y derecho de la imagen.
ASPOSE_ASSERT_EQ(shape->get_Top() + shape->get_Height(), shape->get_Bottom());
ASPOSE_ASSERT_EQ(shape->get_Left() + shape->get_Width(), shape->get_Right());

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPositionSize.docx");
```

## Ver también

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
