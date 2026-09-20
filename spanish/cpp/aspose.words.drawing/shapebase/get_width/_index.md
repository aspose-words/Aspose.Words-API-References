---
title: "Método Aspose::Words::Drawing::ShapeBase::get_Width"
linktitle: "get_Width"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::ShapeBase::get_Width. Obtiene o establece el ancho del bloque contenedor de la forma en C++."
type: docs
weight: 54000
url: /es/cpp/aspose.words.drawing/shapebase/get_width/
---
## ShapeBase::get_Width method


Obtiene o establece el ancho del bloque contenedor de la forma.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Width()
```

## Observaciones


Para una forma de nivel superior, el valor está en puntos.

Para las formas en un grupo, el valor está en el espacio de coordenadas y unidades del grupo padre.

El valor predeterminado es 0.

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


Muestra cómo cambiar el tamaño de una forma con una imagen.
```cpp
// Cuando insertamos una imagen usando el método "InsertImage", el generador escala la forma que muestra la imagen de modo que,
// cuando visualizamos el documento usando un zoom del 100 % en Microsoft Word, la forma muestra la imagen en su tamaño real.
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Una imagen de 400x400 creará un objeto ImageData con un tamaño de imagen de 300x300pt.
System::SharedPtr<Aspose::Words::Drawing::ImageSize> imageSize = shape->get_ImageData()->get_ImageSize();

ASPOSE_ASSERT_EQ(300.0, imageSize->get_WidthPoints());
ASPOSE_ASSERT_EQ(300.0, imageSize->get_HeightPoints());

// Si las dimensiones de una forma coinciden con las dimensiones de los datos de imagen,
// entonces la forma está mostrando la imagen en su tamaño original.
ASPOSE_ASSERT_EQ(300.0, shape->get_Width());
ASPOSE_ASSERT_EQ(300.0, shape->get_Height());

// Reduce el tamaño total de la forma en un 50 %.
System::WithLambda::setter_mul_wrap(GETTER_SETTER_LAMBDA_ARGS(shape, Width), 0.5);

// Los factores de escala se aplican tanto al ancho como a la altura al mismo tiempo para preservar las proporciones de la forma.
ASPOSE_ASSERT_EQ(150.0, shape->get_Width());
ASPOSE_ASSERT_EQ(150.0, shape->get_Height());

// Cuando redimensionamos la forma, el tamaño de los datos de imagen permanece igual.
ASPOSE_ASSERT_EQ(300.0, imageSize->get_WidthPoints());
ASPOSE_ASSERT_EQ(300.0, imageSize->get_HeightPoints());

// Podemos referirnos a las dimensiones de los datos de imagen para aplicar una escala basada en el tamaño de la imagen.
shape->set_Width(imageSize->get_WidthPoints() * 1.1);

ASPOSE_ASSERT_EQ(330.0, shape->get_Width());
ASPOSE_ASSERT_EQ(330.0, shape->get_Height());

doc->Save(get_ArtifactsDir() + u"Image.ScaleImage.docx");
```

## Ver también

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
