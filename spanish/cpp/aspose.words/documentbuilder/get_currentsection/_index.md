---
title: "Aspose::Words::DocumentBuilder::get_CurrentSection método"
linktitle: "get_CurrentSection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::get_CurrentSection método. Obtiene la sección que está actualmente seleccionada en este DocumentBuilder en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words/documentbuilder/get_currentsection/
---
## DocumentBuilder::get_CurrentSection method


Obtiene la sección que está actualmente seleccionada en este [DocumentBuilder](../).

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::DocumentBuilder::get_CurrentSection()
```


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

* Class [Section](../../section/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
