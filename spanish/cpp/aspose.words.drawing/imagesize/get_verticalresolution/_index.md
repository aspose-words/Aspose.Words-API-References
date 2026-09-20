---
title: "Método Aspose::Words::Drawing::ImageSize::get_VerticalResolution"
linktitle: "get_VerticalResolution"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ImageSize::get_VerticalResolution method. Obtiene la resolución vertical en DPI en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.drawing/imagesize/get_verticalresolution/
---
## ImageSize::get_VerticalResolution method


Obtiene la resolución vertical en DPI.

```cpp
double Aspose::Words::Drawing::ImageSize::get_VerticalResolution() const
```


## Ejemplos



Muestra cómo leer las propiedades de una imagen en una forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte una forma en el documento que contenga una imagen tomada de nuestro sistema de archivos local.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Si la forma contiene una imagen, su propiedad ImageData será válida,
// y contendrá un objeto ImageSize.
System::SharedPtr<Aspose::Words::Drawing::ImageSize> imageSize = shape->get_ImageData()->get_ImageSize();

// El objeto ImageSize contiene información de solo lectura sobre la imagen dentro de la forma.
ASSERT_EQ(400, imageSize->get_HeightPixels());
ASSERT_EQ(400, imageSize->get_WidthPixels());

const double delta = 0.05;
ASSERT_NEAR(95.98, imageSize->get_HorizontalResolution(), delta);
ASSERT_NEAR(95.98, imageSize->get_VerticalResolution(), delta);

// Podemos basar el tamaño de la forma en el tamaño de su imagen para evitar estirar la imagen.
shape->set_Width(imageSize->get_WidthPoints() * 2);
shape->set_Height(imageSize->get_HeightPoints() * 2);

doc->Save(get_ArtifactsDir() + u"Drawing.ImageSize.docx");
```

## Ver también

* Class [ImageSize](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
