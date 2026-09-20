---
title: "Método Aspose::Words::PageSetup::get_PageWidth"
linktitle: "get_PageWidth"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::PageSetup::get_PageWidth. Devuelve o establece el ancho de la página en puntos en C++."
type: docs
weight: 36000
url: /es/cpp/aspose.words/pagesetup/get_pagewidth/
---
## PageSetup::get_PageWidth method


Devuelve o establece el ancho de la página en puntos.

```cpp
double Aspose::Words::PageSetup::get_PageWidth()
```


## Ejemplos



Muestra cómo insertar una imagen y usarla como marca de agua.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta la imagen en el encabezado para que sea visible en cada página.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);

// Coloca la imagen en el centro de la página.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Left((builder->get_PageSetup()->get_PageWidth() - shape->get_Width()) / 2);
shape->set_Top((builder->get_PageSetup()->get_PageHeight() - shape->get_Height()) / 2);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertWatermark.docx");
```


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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
