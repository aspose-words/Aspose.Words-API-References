---
title: "Método Aspose::Words::DocumentBuilder::InsertImage"
linktitle: "InsertImage"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DocumentBuilder::InsertImage. Inserta una imagen desde una matriz de bytes en el documento. La imagen se inserta en línea y al 100% de escala en C++."
type: docs
weight: 39000
url: /es/cpp/aspose.words/documentbuilder/insertimage/
---
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&) method


Inserta una imagen desde una matriz de bytes en el documento. La imagen se inserta en línea y al 100 % de escala.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | La matriz de bytes que contiene la imagen. |

### ReturnValue

El nodo de imagen que acaba de insertarse.
## Observaciones


Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el objeto [Shape](../../../aspose.words.drawing/shape/) devuelto por este método.

## Ejemplos



Muestra cómo insertar una imagen desde una matriz de bytes en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// A continuación se presentan tres formas de insertar una imagen desde una matriz de bytes.
// 1 -  Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Forma en línea con dimensiones personalizadas:
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Forma flotante con dimensiones personalizadas:
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserta una imagen desde una matriz de bytes en la posición y tamaño especificados.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | La matriz de bytes que contiene la imagen. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| left | double | Distancia en puntos desde el origen hasta el lado izquierdo de la imagen. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| top | double | Distancia en puntos desde el origen hasta el lado superior de la imagen. |
| ancho | double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| alto | double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| wrapType | Aspose::Words::Drawing::WrapType | Especifica cómo envolver el texto alrededor de la imagen. |

### ReturnValue

El nodo de imagen que acaba de insertarse.
## Observaciones


Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el objeto [Shape](../../../aspose.words.drawing/shape/) devuelto por este método.

## Ejemplos



Muestra cómo insertar una imagen desde una matriz de bytes en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// A continuación se presentan tres formas de insertar una imagen desde una matriz de bytes.
// 1 -  Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Forma en línea con dimensiones personalizadas:
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Forma flotante con dimensiones personalizadas:
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&, double, double) method


Inserta una imagen en línea desde una matriz de bytes en el documento y la escala al tamaño especificado.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes, double width, double height)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | La matriz de bytes que contiene la imagen. |
| ancho | double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| alto | double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |

### ReturnValue

El nodo de imagen que acaba de insertarse.
## Observaciones


Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el objeto [Shape](../../../aspose.words.drawing/shape/) devuelto por este método.

## Ejemplos



Muestra cómo insertar una imagen desde una matriz de bytes en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// A continuación se presentan tres formas de insertar una imagen desde una matriz de bytes.
// 1 -  Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Forma en línea con dimensiones personalizadas:
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Forma flotante con dimensiones personalizadas:
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&) method


Inserta una imagen desde un objeto **Image** en el documento. La imagen se inserta en línea y al 100 % de escala.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | La imagen a insertar en el documento. |

### ReturnValue

El nodo de imagen que acaba de insertarse.
## Observaciones


Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el objeto [Shape](../../../aspose.words.drawing/shape/) devuelto por este método.

## Ejemplos



Muestra cómo insertar una imagen desde un objeto en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// A continuación se presentan tres formas de insertar una imagen desde una instancia de objeto Image.
// 1 -  Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Forma en línea con dimensiones personalizadas:
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Forma flotante con dimensiones personalizadas:
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserta una imagen desde un objeto **Image** en la posición y tamaño especificados.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | La imagen a insertar en el documento. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| left | double | Distancia en puntos desde el origen hasta el lado izquierdo de la imagen. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| top | double | Distancia en puntos desde el origen hasta el lado superior de la imagen. |
| ancho | double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| alto | double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| wrapType | Aspose::Words::Drawing::WrapType | Especifica cómo envolver el texto alrededor de la imagen. |

### ReturnValue

El nodo de imagen que acaba de insertarse.
## Observaciones


Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el objeto [Shape](../../../aspose.words.drawing/shape/) devuelto por este método.

## Ejemplos



Muestra cómo insertar una imagen desde un objeto en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// A continuación se presentan tres formas de insertar una imagen desde una instancia de objeto Image.
// 1 -  Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Forma en línea con dimensiones personalizadas:
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Forma flotante con dimensiones personalizadas:
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&, double, double) method


Inserta una imagen en línea desde un objeto **Image** en el documento y la escala al tamaño especificado.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image, double width, double height)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | La imagen a insertar en el documento. |
| ancho | double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| alto | double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |

### ReturnValue

El nodo de imagen que acaba de insertarse.
## Observaciones


Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el objeto [Shape](../../../aspose.words.drawing/shape/) devuelto por este método.

## Ejemplos



Muestra cómo insertar una imagen desde un objeto en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// A continuación se presentan tres formas de insertar una imagen desde una instancia de objeto Image.
// 1 -  Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Forma en línea con dimensiones personalizadas:
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Forma flotante con dimensiones personalizadas:
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&) method


Inserta una imagen desde un flujo en el documento. La imagen se inserta en línea y al 100 % de escala.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| flujo | const System::SharedPtr\<System::IO::Stream\>\& | El flujo que contiene la imagen. |

### ReturnValue

El nodo de imagen que acaba de insertarse.
## Observaciones


Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el objeto [Shape](../../../aspose.words.drawing/shape/) devuelto por este método.

## Ejemplos



Muestra cómo insertar una imagen desde un flujo en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // A continuación se presentan tres formas de insertar una imagen desde un flujo.
    // 1 -  Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 -  Forma en línea con dimensiones personalizadas:
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 -  Forma flotante con dimensiones personalizadas:
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```


Muestra cómo insertar una forma con una imagen desde un flujo en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    builder->Write(u"Image from stream: ");
    builder->InsertImage(stream);
}

doc->Save(get_ArtifactsDir() + u"Image.FromStream.docx");
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserta una imagen desde un flujo en la posición y tamaño especificados.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| flujo | const System::SharedPtr\<System::IO::Stream\>\& | El flujo que contiene la imagen. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| left | double | Distancia en puntos desde el origen hasta el lado izquierdo de la imagen. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| top | double | Distancia en puntos desde el origen hasta el lado superior de la imagen. |
| ancho | double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| alto | double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| wrapType | Aspose::Words::Drawing::WrapType | Especifica cómo envolver el texto alrededor de la imagen. |

### ReturnValue

El nodo de imagen que acaba de insertarse.
## Observaciones


Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el objeto [Shape](../../../aspose.words.drawing/shape/) devuelto por este método.

## Ejemplos



Muestra cómo insertar una imagen desde un flujo en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // A continuación se presentan tres formas de insertar una imagen desde un flujo.
    // 1 -  Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 -  Forma en línea con dimensiones personalizadas:
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 -  Forma flotante con dimensiones personalizadas:
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&, double, double) method


Inserta una imagen en línea desde un flujo en el documento y la escala al tamaño especificado.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream, double width, double height)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| flujo | const System::SharedPtr\<System::IO::Stream\>\& | El flujo que contiene la imagen. |
| ancho | double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| alto | double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |

### ReturnValue

El nodo de imagen que acaba de insertarse.
## Observaciones


Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el objeto [Shape](../../../aspose.words.drawing/shape/) devuelto por este método.

## Ejemplos



Muestra cómo insertar una imagen desde un flujo en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // A continuación se presentan tres formas de insertar una imagen desde un flujo.
    // 1 -  Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 -  Forma en línea con dimensiones personalizadas:
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 -  Forma flotante con dimensiones personalizadas:
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&) method


Inserta una imagen desde un archivo o URL en el documento. La imagen se inserta en línea y al 100 % de escala.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | const System::String\& | El archivo con la imagen. Puede ser cualquier URI local o remoto válido. |

### ReturnValue

El nodo de imagen que acaba de insertarse.
## Observaciones


Esta sobrecarga descargará automáticamente la imagen antes de insertarla en el documento si se especifica un URI remoto.

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el objeto [Shape](../../../aspose.words.drawing/shape/) devuelto por este método.

## Ejemplos



Muestra cómo insertar una imagen desde el sistema de archivos local en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A continuación se presentan tres formas de insertar una imagen desde un nombre de archivo del sistema local.
// 1 -  Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Forma en línea con dimensiones personalizadas:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Forma flotante con dimensiones personalizadas:
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```


Muestra cómo determinar qué imagen se insertará.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"Scalable Vector Graphics.svg");

// Aspose.Words inserta una imagen SVG en el documento como PNG con la extensión svgBlip
// que contiene la representación vectorial original de la imagen SVG.
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// Aspose.Words inserta una imagen SVG en el documento como PNG, al igual que Microsoft Word lo hace para el formato antiguo.
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.Svg.doc");

doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);

// Aspose.Words inserta una imagen SVG en el documento como metafile EMF para mantener la imagen en representación vectorial.
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.Emf.docx");
```


Muestra cómo insertar una imagen gif en el documento.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// Podemos insertar una imagen gif usando una ruta o una matriz de bytes.
// Funciona solo si DocumentBuilder está optimizado para la versión 2010 de Word o superior.
// Nota, que el acceso a los bytes de la imagen provoca la conversión de Gif a Png.
System::SharedPtr<Aspose::Words::Drawing::Shape> gifImage = builder->InsertImage(get_ImageDir() + u"Graphics Interchange Format.gif");

gifImage = builder->InsertImage(System::IO::File::ReadAllBytes(get_ImageDir() + u"Graphics Interchange Format.gif"));

builder->get_Document()->Save(get_ArtifactsDir() + u"InsertGif.docx");
```


Muestra cómo insertar una forma con una imagen en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A continuación se presentan dos ubicaciones donde el método "InsertShape" del document builder
// puede obtener la imagen que la forma mostrará.
// 1 -  Pase un nombre de archivo del sistema de archivos local de una imagen:
builder->Write(u"Image from local file: ");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->Writeln();

// 2 -  Pase una URL que apunte a una imagen.
builder->Write(u"Image from a URL: ");
builder->InsertImage(get_ImageUrl());
builder->Writeln();

doc->Save(get_ArtifactsDir() + u"Image.FromUrl.docx");
```


Muestra cómo insertar una imagen flotante en el centro de una página.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta una imagen flotante que aparecerá detrás del texto superpuesto y alinéala al centro de la página.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```


Muestra cómo insertar una imagen WebP.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"WebP image.webp");

doc->Save(get_ArtifactsDir() + u"Image.InsertWebpImage.docx");
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserta una imagen desde un archivo o URL en la posición y tamaño especificados.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | const System::String\& | El archivo que contiene la imagen. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| left | double | Distancia en puntos desde el origen hasta el lado izquierdo de la imagen. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| top | double | Distancia en puntos desde el origen hasta el lado superior de la imagen. |
| ancho | double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| alto | double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| wrapType | Aspose::Words::Drawing::WrapType | Especifica cómo envolver el texto alrededor de la imagen. |

### ReturnValue

El nodo de imagen que acaba de insertarse.
## Observaciones


Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el objeto [Shape](../../../aspose.words.drawing/shape/) devuelto por este método.

## Ejemplos



Muestra cómo insertar una imagen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Hay dos formas de usar un document builder para obtener una imagen y luego insertarla como una forma flotante.
// 1 -  Desde un archivo en el sistema de archivos local:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 0.0, 200.0, 200.0, Aspose::Words::Drawing::WrapType::Square);

// 2 -  Desde una URL:
builder->InsertImage(get_ImageUrl(), Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 250.0, 200.0, 200.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFloatingImage.docx");
```


Muestra cómo insertar una imagen del sistema de archivos local en un documento mientras se preservan sus dimensiones.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// El método InsertImage crea una forma flotante con la imagen pasada en sus datos de imagen.
// Podemos especificar las dimensiones de la forma pasándolas a este método.
System::SharedPtr<Aspose::Words::Drawing::Shape> imageShape = builder->InsertImage(get_ImageDir() + u"Logo.jpg", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 0.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 0.0, -1.0, -1.0, Aspose::Words::Drawing::WrapType::Square);

// Pasar valores negativos como dimensiones previstas definirá automáticamente
// las dimensiones de la forma basándose en las dimensiones de su imagen.
ASPOSE_ASSERT_EQ(300.0, imageShape->get_Width());
ASPOSE_ASSERT_EQ(300.0, imageShape->get_Height());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertImageOriginalSize.docx");
```


Muestra cómo insertar una imagen desde el sistema de archivos local en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A continuación se presentan tres formas de insertar una imagen desde un nombre de archivo del sistema local.
// 1 -  Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Forma en línea con dimensiones personalizadas:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Forma flotante con dimensiones personalizadas:
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&, double, double) method


Inserta una imagen en línea desde un archivo o URL en el documento y la escala al tamaño especificado.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName, double width, double height)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | const System::String\& | El archivo que contiene la imagen. |
| ancho | double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| alto | double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |

### ReturnValue

El nodo de imagen que acaba de insertarse.
## Observaciones


Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el objeto [Shape](../../../aspose.words.drawing/shape/) devuelto por este método.

## Ejemplos



Muestra cómo insertar una imagen desde el sistema de archivos local en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A continuación se presentan tres formas de insertar una imagen desde un nombre de archivo del sistema local.
// 1 -  Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Forma en línea con dimensiones personalizadas:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Forma flotante con dimensiones personalizadas:
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream)
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&, double, double) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream, double width, double height)
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
