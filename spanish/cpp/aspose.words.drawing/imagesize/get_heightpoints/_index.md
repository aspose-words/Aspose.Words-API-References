---
title: "Método Aspose::Words::Drawing::ImageSize::get_HeightPoints"
linktitle: "get_HeightPoints"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ImageSize::get_HeightPoints method. Obtiene la altura de la imagen en puntos. 1 punto es 1/72 de pulgada en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.drawing/imagesize/get_heightpoints/
---
## ImageSize::get_HeightPoints method


Obtiene la altura de la imagen en puntos. 1 punto es 1/72 de pulgada.

```cpp
double Aspose::Words::Drawing::ImageSize::get_HeightPoints()
```


## Ejemplos



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

* Class [ImageSize](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
